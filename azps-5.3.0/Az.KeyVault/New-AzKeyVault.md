---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491960"
---
# New-AzKeyVault

## SYNOPSIS
키 자격 증명 모음을 만듭니다.

## 구문

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzKeyVault** cmdlet은 지정된 리소스 그룹에 키 자격 증명 모음을 만듭니다. 이 cmdlet은 키 자격 증명 모음에서 키와 비밀을 추가, 제거 또는 나열할 수 있는 권한을 현재 로그온한 사용자에게 부여합니다.
참고: 새 키 자격 증명 모음을 만들려고 할 때 **구독이 'Microsoft.KeyVault'** 네임스페이스를 사용하기 위해 등록되지 않은 경우 **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"를** 실행한 다음 **New-AzKeyVault** 명령을 다시 실행합니다. 자세한 내용은 Register-AzResourceProvider를 참조하세요.

## 예제

### 예제 1: 표준 키 자격 증명 모음 만들기
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

이 명령은 미국 동부 Azure 지역에 Contoso03Vault라는 키 자격 증명 모음을 만듭니다. 이 명령은 Group14라는 리소스 그룹에 키 자격 증명 모음을 추가합니다. 이 명령은 SKU 매개 변수에 대한 값을 *지정하지* 않습니다. 이 명령은 표준 키 자격 증명 모음을 만듭니다.

### 예제 2: 프리미엄 키 자격 증명 모음 만들기
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

이 명령은 이전 예제와 마찬가지로 키 자격 증명 모음을 만듭니다. 그러나 프리미엄 키 자격 증명 모음을 만드는 *SKU* 매개 변수에 대한 프리미엄 값을 지정합니다.

### 예제 3
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

키 자격 증명 모음을 만들고 가상 네트워크에서 지정된 IP 주소에 대한 액세스를 허용하는 네트워크 규칙을 $myNetworkResId. 자세한 `New-AzKeyVaultNetworkRuleSetObject` 내용은 다음을 참조하세요.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
예를 들어 가상 머신을 만들 때 이 키 자격 증명 모음이 리소스 생성에서 참조될 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀을 검색할 수 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Azure 디스크 암호화 서비스를 사용하면 이 키 자격 증명 모음에서 비밀을 얻을 수 있으며 키 래프를 래프할 수 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
이 키 자격 증명 모음이 템플릿 배포에서 참조될 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀을 얻을 수 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnablePurgeProtection
지정된 경우 이 자격 증명 모음에 대해 즉시 지우기 방지를 사용하도록 설정됩니다. 소프트 삭제도 사용하도록 설정해야 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableRbacAuthorization
지정된 경우 RBAC(역할 기반 액세스 제어)에 의해 데이터 작업에 권한을 부여할 수 있으며 자격 증명 모음 속성에 지정된 액세스 정책은 무시됩니다. 관리 작업은 항상 RBAC를 통해 권한이 부여됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
키 자격 증명 모음을 만들 Azure 지역을 지정합니다. [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 명령을 사용하여 선택을 볼 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
만들 키 자격 증명 모음의 이름을 지정합니다. 이름은 문자, 숫자 또는 하이픈의 조합일 수 있습니다. 이름은 문자 또는 숫자로 시작하고 끝나야 합니다. 이름은 범용적으로 고유해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
자격 증명 모음의 네트워크 규칙 집합을 지정합니다. 특정 네트워크 위치에서 키 자격 증명 모음의 접근성을 제어합니다. `New-AzKeyVaultNetworkRuleSetObject`.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
키 자격 증명 모음 인스턴스의 SKU를 지정합니다. 각 SKU에 사용할 수 있는 기능에 대한 자세한 내용은 Azure Key Vault 가격 책정 웹 https://go.microsoft.com/fwlink/?linkid=512521) 사이트(.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SoftDeleteRetentionInDays
삭제된 리소스가 보존되는 기간과 삭제된 상태의 자격 증명 모음 또는 개체를 삭제할 수 있는 기간을 지정합니다. 기본값은 90일입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
해시 테이블 형식의 키-값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Management.Automation.SwitchParameter

### Microsoft.Azure.Management.KeyVault.Models.SkuName

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

## 참고 사항

## 관련 링크

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVault](./Remove-AzKeyVault.md)
