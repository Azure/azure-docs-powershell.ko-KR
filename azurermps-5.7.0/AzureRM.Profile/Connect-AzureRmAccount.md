---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525036"
---
# Connect-AzureRmAccount

## SYNOPSIS
Azure Resource Manager cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### UserWithSubscriptionId (기본값)
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Connect-AzureRmAccount cmdlet은 Azure 리소스 관리자 cmdlet 요청과 함께 사용할 인증 된 계정으로 Azure에 연결 합니다.

이 인증 된 계정은 Azure Resource Manager cmdlet 에서만 사용할 수 있습니다.

서비스 관리 cmdlet에 사용할 인증 된 계정을 추가 하려면 Add-AzureAccount 또는 Import-AzurePublishSettingsFile cmdlet을 사용 합니다.

이 cmdlet을 실행 한 후에는 AzureRmAccount을 사용 하 여 Azure 계정에서 연결을 끊을 수 있습니다.

## 예제의

### 예제 1: 대화형 로그인을 사용 하 여 Azure 계정에 연결
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

이 명령은 Azure 계정에 연결 됩니다.

이 계정으로 Azure Resource Manager cmdlet을 실행 하려면 프롬프트에서 Microsoft 계정 또는 조직 ID 자격 증명을 제공 해야 합니다.

자격 증명에 multi-factor authentication을 사용할 수 있는 경우 대화형 옵션을 사용 하 여 로그인 하거나 서비스 사용자 인증을 사용 해야 합니다.

### 예제 2: 조직 ID 자격 증명을 사용 하 여 Azure 계정에 연결
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.

두 번째 명령은 $Credential에 저장 된 자격 증명을 사용 하 여 Azure 계정에 연결 합니다.

이 계정은 조직 ID 자격 증명을 사용 하 여 Azure Resource Manager를 인증 합니다.

이 계정을 사용 하 여 Azure Resource Manager cmdlet을 실행 하는 데 multi-factor authentication 또는 Microsoft 계정 자격 증명을 사용할 수 없습니다.

### 예제 3: Azure service principal 계정에 연결
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

첫 번째 명령은 사용자 자격 증명을 가져온 다음 $Credential 변수에 저장 합니다.

두 번째 명령은 지정 된 테 넌 트에 대해 $Credential에 저장 된 서비스 사용자 자격 증명을 사용 하 여 Azure에 연결 합니다.

ServicePrincipal switch 매개 변수는 계정이 서비스 사용자로 인증 됨을 나타냅니다.

### 예제 4: 대화형 로그인을 사용 하 여 특정 테 넌 트 및 구독에 대 한 계정에 연결
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

이 명령은 Azure 계정에 연결 하 고, 지정 된 테 넌 트 및 구독에 대 한 cmdlet을 기본적으로 실행 하도록 AzureRM PowerShell을 구성 합니다.

### 예제 5: 관리 서비스 Id 로그인을 사용 하 여 계정 추가
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

이 명령은 호스트 환경의 관리 되는 서비스 id를 사용 하 여 기록 합니다 (예: 지정 된 관리 되는 서비스 Id를 사용 하 여 VirtualMachine에서 실행 되는 경우 해당 id를 사용 하 여 코드에 로그인 할 수 있음)

## 변수

### -AccessToken
액세스 토큰을 지정 합니다.

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
액세스 토큰의 계정 Id

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
수단

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
인증서 해시 (지문)

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -컨텍스트 이름
이 로그인의 기본 컨텍스트 이름입니다.  로그인 후이 이름을 기준으로이 컨텍스트를 선택할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
PSCredential 개체를 지정 합니다.
PSCredential 개체에 대 한 자세한 내용을 보려면 Get-Help 가져오기-자격 증명을 입력 합니다.

PSCredential 개체는 조직 ID 자격 증명 또는 서비스 사용자 자격 증명에 대 한 응용 프로그램 ID 및 비밀에 대 한 사용자 ID 및 암호를 제공 합니다.

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -환경
로그인 하는 계정이 포함 된 환경

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Graph 서비스에 대 한 AccessToken

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
현재 환경에서 관리 서비스 id를 사용 하 여 로그인 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken
KeyVault 서비스에 대 한 AccessToken

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName
관리 서비스 로그인에 대 한 호스트 이름

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort
관리 서비스 로그인의 포트 번호

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -범위
컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.

```yaml
Type: ContextModificationScope
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
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipValidation
액세스 토큰에 대 한 유효성 검사 건너뛰기

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -구독
구독 이름 또는 ID

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TenantId
선택적 테 넌 트 이름 또는 ID

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 이름
' SubscriptionId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.

### 이름
' SubscriptionName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.

## 출력

### PSAzureProfile
로그인 한 사용자에 대 한 자격 증명, 구독, 계정 및 테 넌 트 정보

## 상속자

## 관련 링크

