using System;
using System.Windows.Forms;
using GTA;
using GTA.Math;
using GTA.Native;

public class Vehicle_360 : Script
{
    Keys ThreeSixtyButton;

    public Vehicle_360()
    {
        ThreeSixtyButton = Settings.GetValue<Keys>("Options", "ThreeSixtyButton", Keys.D3);

        KeyUp += OnKeyUp;
    }

    private void OnKeyUp(object sender, KeyEventArgs e)
    {
        if (e.KeyCode == ThreeSixtyButton)
        {
            Ped playerPed = Game.Player.Character;

            if (playerPed.IsAlive && playerPed.IsInVehicle())
            {
                Vehicle veh = playerPed.CurrentVehicle;

                if (veh.Model.IsCar)
                {
                    veh.ApplyForce(new Vector3(8f, 5.5f, 0f), new Vector3(8f, 0f, 0f), ForceType.MaxForceRot);
                }
            }
        }
    }
}
