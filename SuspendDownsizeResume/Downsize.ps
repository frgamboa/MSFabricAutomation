$tenantId = "From microsoft Entra"
$clientId = "From the App registered in microsoft Entra"
$clientSecret = "From the App registered in microsoft Entra" 
$resourceGroup = "Resource Group"
$FabricCapacity = "Fabric Cpacity Name"
$sku = "F4"
$uri = "https://management.azure.com/subscriptions/"+ $subscription+ "/resourceGroups/"+$resourceGroup+"/providers/Microsoft.Fabric/capacities/" + $FabricCapacity

$body = @{
    grant_type    = "client_credentials"
    client_id     = $clientId
    client_secret = $clientSecret
    resource      = "https://management.azure.com/"
}


try {
    $tokenResponse = Invoke-RestMethod -Method Post -Uri "https://login.microsoftonline.com/$tenantId/oauth2/token" -ContentType "application/x-www-form-urlencoded" -Body $body
    $accessToken = $tokenResponse.access_token

    # Headers for the PATCH request
    $headers = @{
        Authorization = "Bearer $accessToken"
        "Content-Type" = "application/json"
    }
}
Catch{
    Write-Error "An error occurred: $_"
}

$uri = $uri+"?api-version=2023-11-01"
$method = "Patch"
$body = @{
    properties = @{
        administration = @{
            # Add your administration properties here
        }
    }
    sku = @{
        name = $sku
        tier = "Fabric"
    }
    tags = @{
        # Add your resource tags here
    }
} | ConvertTo-Json

try{
    $response = Invoke-RestMethod -Method $method -Uri $uri -Headers $headers -Body $body
    # Output the response
    if ($response) {
        $response
    } else {
        Write-Output "No content returned in the response."
    }
}
Catch{
    Write-Error "An error occurred: $_"
}
