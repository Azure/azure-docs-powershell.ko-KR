---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333261"
---
# Connect-AzAccount

## SYNOPSIS
Az PowerShell 모듈의 cmdlet과 함께 사용하기 위해 인증된 계정으로 Azure에 연결합니다.

## 구문

### UserWithSubscriptionId(기본값)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명

이 cmdlet은 Az PowerShell 모듈의 cmdlet과 함께 사용하기 위해 인증된 계정으로 `Connect-AzAccount` Azure에 연결합니다. 이 인증된 계정은 Azure Resource Manager 요청에만 사용할 수 있습니다. 서비스 관리에 사용할 인증된 계정을 추가하려면 Azure PowerShell 모듈의 `Add-AzureAccount` cmdlet을 사용합니다. 현재 사용자에 대한 컨텍스트가 없는 경우 사용자의 컨텍스트 목록은 처음 25개 구독 각각에 대한 컨텍스트로 채워진 것입니다.
사용자에 대해 만든 컨텍스트 목록은 다음을 실행하여 찾을 수 `Get-AzContext -ListAvailable` 있습니다. 이 컨텍스트 인구를 건너뛰기 위해 **SkipContextPopulation** 스위치 매개 변수를 지정합니다. 이 cmdlet을 실행한 후 다음을 사용하여 Azure 계정에서 연결을 끊을 수 `Disconnect-AzAccount` 있습니다.

## 예제

### 예제 1: Azure 계정에 연결

이 예제는 Azure 계정에 연결합니다. Microsoft 계정 또는 조직 ID 자격 증명을 제공해야 합니다. 자격 증명에 다단계 인증을 사용하도록 설정한 경우 대화형 옵션을 사용하여 로그인하거나 서비스 주체 인증을 사용해야 합니다.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 2: (Windows PowerShell 5.1만 해당) 조직 ID 자격 증명을 사용하여 Azure에 연결

이 시나리오는 Windows PowerShell 5.1에서만 작동합니다. 첫 번째 명령은 사용자 자격 증명을 묻는 메시지를 표시하고 변수에 `$Credential` 저장합니다. 두 번째 명령은 에 저장된 자격 증명을 사용하여 Azure 계정에 `$Credential` 연결합니다. 이 계정은 조직 ID 자격 증명을 사용하여 Azure에서 인증합니다.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 3: 서비스 주체 계정을 사용하여 Azure에 연결

첫 번째 명령은 서비스 주체 자격 증명을 묻는 메시지를 표시하고 변수에 `$Credential` 저장합니다. 메시지가 표시될 때 사용자 이름 및 서비스 주체 암호에 대한 애플리케이션 ID를 암호로 입력합니다. 두 번째 명령은 변수에 저장된 서비스 주체 자격 증명을 사용하여 지정된 Azure 테넌트에 `$Credential` 연결합니다. **ServicePrincipal** 스위치 매개 변수는 계정이 서비스 주체로 인증하는지 나타냅니다.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 4: 대화형 로그인을 사용하여 특정 테넌트 및 구독에 연결

이 예제에서는 지정된 테넌트 및 구독을 사용하여 Azure 계정에 연결합니다.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 5: 관리 서비스 ID를 사용하여 연결

이 예제에서는 호스트 환경의 MSI(관리 서비스 ID)를 사용하여 연결합니다. 예를 들어 MSI가 할당된 가상 머신에서 Azure에 로그인합니다.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 6: 관리 서비스 ID 로그인 및 ClientId를 사용하여 연결

이 예제에서는 **myUserAssignedIdentity의** 관리 서비스 ID를 사용하여 연결합니다. 가상 머신에 사용자 할당 ID를 추가한 다음 사용자 할당 ID의 ClientId를 사용하여 연결합니다. 자세한 내용은 Azure VM에서 Azure 리소스에 대한 관리 ID [구성을 참조하세요.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 7: 인증서를 사용하여 연결

이 예제에서는 인증서 기반 서비스 주체 인증을 사용하여 Azure 계정에 연결합니다.
인증에 사용되는 서비스 주체는 지정된 인증서로 만들어야 합니다. 자체 서명된 인증서를 만들고 권한을 할당하는 자세한 내용은 Azure PowerShell을 사용하여 인증서로 서비스 주체 [만들기를 참조하세요.](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## PARAMETERS

### -AccessToken

액세스 토큰을 지정합니다.

> [!CAUTION]
> 액세스 토큰은 자격 증명의 유형입니다. 기밀을 유지하기 위해 적절한 보안 예방 조치를 취해야 합니다. 또한 액세스 토큰은 시간 제한이 있으며 장기 실행 작업이 완료되지 않을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId

**AccessToken** 매개 변수 집합의 액세스 토큰에 대한 계정 ID입니다. **ManagedService** 매개 변수 집합의 관리되는 서비스에 대한 계정 ID입니다. 관리되는 서비스 리소스 ID 또는 연결된 클라이언트 ID일 수 있습니다.
시스템 할당 ID를 사용 중이면 이 필드를 비워 두십시오.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

서비스 주체의 애플리케이션 ID입니다.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint

인증서 해시 또는 지문입니다.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContextName

이 로그인에 대한 기본 Azure 컨텍스트의 이름입니다. Azure 컨텍스트에 대한 자세한 내용은 [Azure PowerShell 컨텍스트 개체를 참조하세요.](/powershell/azure/context-persistence)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential

**PSCredential** 개체를 지정합니다. **PSCredential** 개체에 대한 자세한 내용은 `Get-Help Get-Credential` .를 입력합니다. **PSCredential** 개체는 조직 ID 자격 증명에 대한 사용자 ID 및 암호 또는 서비스 주체 자격 증명에 대한 애플리케이션 ID 및 비밀을 제공합니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile

Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Environment

Azure 계정을 포함하는 환경입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

메시지를 표시하지 않고 동일한 이름으로 기존 컨텍스트를 덮어 덮어 습니다.

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

### -GraphAccessToken

Graph Service용 AccessToken입니다.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity

관리 서비스 ID를 사용하여 로그인합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken

KeyVault Service에 대한 AccessToken입니다.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName

사용되지 않습니다. 사용자 지정된 MSI 엔드포인트를 사용 설정하기 위해 환경 변수를 MSI_ENDPOINT"를 http://localhost:50342/oauth2/token 지정합니다. 관리되는 서비스의 호스트 이름입니다.

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort

사용되지 않습니다. 사용자 지정된 MSI 엔드포인트를 사용 설정하기 위해 환경 변수를 MSI_ENDPOINT"를 http://localhost:50342/oauth2/token 지정합니다. 관리되는 서비스의 포트 번호입니다.

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret

사용되지 않습니다. 사용자 지정된 MSI 비밀을 사용 설정하기 위해 환경 변수를 MSI_SECRET. 관리되는 서비스 로그인에 대한 토큰입니다.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxContextPopulation

로그인 후 컨텍스트를 채우는 최대 구독 번호입니다. 기본값은 25입니다. 컨텍스트에 대한 모든 구독을 채우기 위해 -1로 설정하세요.

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

### -Scope

컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal

서비스 주체 자격 증명을 제공하여 이 계정이 인증을 하게 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipContextPopulation

컨텍스트가 없는 경우 컨텍스트 인구를 건너뜁.

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

### -SkipValidation

액세스 토큰에 대한 유효성 검사 건너뛰기

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subscription

구독 이름 또는 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tenant

선택적 테넌트 이름 또는 ID입니다.

> [!NOTE]
> 현재 API의 제한 사항으로 인해 B2B(기업간) 계정으로 연결할 때 테넌트 이름 대신 테넌트 ID를 사용해야 합니다.

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication

브라우저 컨트롤 대신 디바이스 코드 인증을 사용합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## 참고 사항

## 관련 링크
