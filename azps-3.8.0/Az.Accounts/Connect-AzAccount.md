---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 32a5c4ac20d584c26d95724a3f4ab4630504fb6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043031"
---
# Connect-AzAccount

## SYNOPSIS
Az PowerShell 모듈에서 cmdlet과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.

## 구문과

### UserWithSubscriptionId (기본값)

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은

이 `Connect-AzAccount` cmdlet은 Az PowerShell 모듈에서 cmdlet과 함께 사용할 수 있도록 인증 된 계정을 사용 하 여 Azure에 연결 합니다. Azure Resource Manager 요청과 함께이 인증 된 계정을 사용할 수 있습니다. 서비스 관리에 사용할 인증 된 계정을 추가 하려면 `Add-AzureAccount` Azure PowerShell 모듈에서 cmdlet을 사용 합니다. 현재 사용자에 대 한 컨텍스트를 찾을 수 없는 경우 사용자의 컨텍스트 목록은 처음 25 개의 각 구독에 대 한 컨텍스트로 채워집니다.
사용자에 대해 생성 된 컨텍스트 목록은를 실행 하 여 찾을 수 있습니다 `Get-AzContext -ListAvailable` . 이 컨텍스트 채우기를 건너뛰려면 **Skipcontextpopulation** 스위치 매개 변수를 지정 합니다. 이 cmdlet을 실행 한 후를 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다 `Disconnect-AzAccount` .

## 예제의

### 예제 1: Azure 계정에 연결

이 예제에서는 Azure 계정에 연결 합니다. Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다. 자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 2: (Windows PowerShell 5.1에만 해당) 조직 ID 자격 증명을 사용 하 여 Azure에 연결

이 시나리오는 Windows PowerShell 5.1 에서만 작동 합니다. 첫 번째 명령은 사용자 자격 증명을 묻는 메시지를 표시 하 고 변수에 저장 합니다 `$Credential` . 두 번째 명령은에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다 `$Credential` . 이 계정은 조직 ID 자격 증명을 사용 하 여 Azure를 인증 합니다.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 3: 서비스 사용자 계정을 사용 하 여 Azure에 연결

첫 번째 명령은 사용자 자격 증명을 입력 하 라는 메시지를 표시 하 고 변수에 저장 합니다 `$Credential` . 메시지가 표시 되 면 사용자 이름 및 서비스 사용자 암호에 대 한 응용 프로그램 ID를 암호로 입력 합니다. 두 번째 명령은 변수에 저장 된 서비스 사용자 자격 증명을 사용 하 여 지정 된 Azure 테 넌 트를 연결 합니다 `$Credential` . **Serviceprincipal** switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 연결

이 예제에서는 지정 된 테 넌 트 및 구독을 사용 하 여 Azure 계정에 연결 합니다.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 5: 관리 서비스 Id를 사용 하 여 연결

이 예제에서는 호스트 환경의 MSI (관리 서비스 Id)를 사용 하 여 연결 합니다. 예를 들어 MSI를 할당 한 가상 컴퓨터에서 Azure에 로그인 합니다.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### 예제 6: 관리 서비스 Id 로그인 및 ClientId를 사용 하 여 연결

이 예제에서는 **myUserAssignedIdentity** 의 관리 되는 서비스 id를 사용 하 여 연결 합니다. 사용자가 할당 한 id를 가상 컴퓨터에 추가 하 고 사용자가 할당 한 id의 ClientId를 사용 하 여 연결 합니다. 자세한 내용은 [AZURE VM에서 azure 리소스의 관리 되는 Id 구성을](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)참조 하세요.

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

### 예제 7: 인증서를 사용 하 여 연결

이 예제에서는 인증서 기반 서비스 사용자 인증을 사용 하 여 Azure 계정에 연결 합니다.
인증에 사용 되는 서비스 사용자를 지정 된 인증서를 사용 하 여 만들어야 합니다. 자체 서명 된 인증서를 만들고 사용 권한을 할당 하는 방법에 대 한 자세한 내용은 [Azure PowerShell을 사용 하 여 인증서로 서비스 사용자 만들기를](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) 참조 하세요.

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

## 변수

### -AccessToken

액세스 토큰을 지정 합니다.

> [!CAUTION]
> 액세스 토큰은 자격 증명의 유형입니다. 적절 한 보안 예방 조치를 사용 하 여 기밀을 유지 해야 합니다. 또한 액세스 토큰은 시간 제한을 초과 하며 장기 실행 작업이 완료 되지 못하게 할 수 있습니다.

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

**AccessToken** 매개 변수 집합의 액세스 토큰에 대 한 계정 ID입니다. **Managedservice** 매개 변수 집합의 관리 서비스에 대 한 계정 ID입니다. 관리 서비스 리소스 ID 또는 연결 된 클라이언트 ID 일 수 있습니다.
시스템에 할당 된 id를 사용 하려면이 필드를 비워 둡니다.

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

서비스 사용자의 응용 프로그램 ID입니다.

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

인증서 해시 또는 지문.

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

### -컨텍스트 이름

이 로그인에 대 한 기본 Azure 컨텍스트의 이름입니다. Azure 컨텍스트에 대 한 자세한 내용은 [Azure PowerShell 컨텍스트 개체](/powershell/azure/context-persistence)를 참조 하세요.

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

**PSCredential** 개체를 지정 합니다. **PSCredential** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Credential` 합니다. **PSCredential** 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 id 및 비밀에 대 한 사용자 id 및 암호를 제공 합니다.

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

Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -환경

Azure 계정을 포함 하는 환경입니다.

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

메시지를 표시 하지 않고 같은 이름으로 기존 컨텍스트를 덮어씁니다.

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

Graph 서비스에 대 한 AccessToken.

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

### -Id

관리 서비스 Id를 사용 하 여 로그인 합니다.

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

KeyVault 서비스에 대 한 AccessToken.

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

관리 서비스의 호스트 이름입니다.

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

관리 서비스의 포트 번호입니다.

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

### -Managed서비스 Ecret

관리 서비스 로그인에 대 한 토큰입니다.

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

### -범위

컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.

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

이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.

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

컨텍스트를 찾을 수 없는 경우 컨텍스트 채우기를 건너뜁니다.

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

액세스 토큰에 대 한 유효성 검사를 건너뜁니다.

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

### -구독

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

### -테 넌 트

선택적 테 넌 트 이름 또는 ID입니다.

> [!NOTE]
> 현재 API의 제한 사항으로 인해 B2B (비즈니스 간) 계정으로 연결할 때 테 넌 트 이름 대신 테 넌 트 ID를 사용 해야 합니다.

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

브라우저 컨트롤 대신 디바이스 코드 인증을 사용 합니다. PowerShell 버전 6 이상에 대 한 기본 인증 유형입니다.

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

### -확인

Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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

Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.
(http://go.microsoft.com/fwlink/?LinkID=113216).

## 입력

### System. 문자열

## 출력

### Microsoft. Azure. a PSAzureProfile

## 상속자

## 관련 링크
