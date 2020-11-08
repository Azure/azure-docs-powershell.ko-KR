---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046396"
---
# Add-AzureAccount

## SYNOPSIS
Windows PowerShell에 Azure 계정을 추가 합니다.

## 구문과

### 사용자 (기본값)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
Windows PowerShell에서 Azure 계정 및 해당 구독을 사용할 수 있도록 **추가-azureaccount** cmdlet을 수행 합니다.
Windows PowerShell에서 Azure 계정으로 로그인 하는 것과 같습니다.
계정에서 로그 아웃 하려면 **제거-AzureAccount** cmdlet을 사용 합니다.

**-Azureaccount** Azure 계정에 대 한 정보를 다운로드 하 고 로밍 사용자 프로필의 구독 데이터 파일에 저장 합니다.
또한 Windows PowerShell에서 사용자 대신 Azure 계정에 액세스할 수 있도록 하는 액세스 토큰을 가져옵니다.
명령이 완료 되 면 Windows PowerShell에서 Azure 계정을 관리할 수 있습니다.

Azure 계정을 Windows PowerShell에서 사용할 수 있도록 하는 방법에는 두 가지 방법이 있습니다.
Azure AD (azure Active Directory) 인증 액세스 토큰 또는 관리 인증서를 사용 하는 **가져오기-Azureaccount Settingsfile** 을 사용 하는 **추가-azureaccount** cmdlet을 사용할 수 있습니다.
사용할 방법에 대 한 지침은 [방법: 구독에 연결](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ()을 참조 하세요 https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

**-AzureAccount** 를 실행 하면 Azure 계정에 로그인 하 라는 메시지가 대화형 창으로 표시 됩니다.
이 로그인은 액세스 토큰이 만료 될 때까지 유효 합니다.
만료 되는 경우 계정에 액세스 해야 하는 cmdlet **은 추가 AzureAccount** 를 다시 실행 하 라는 메시지를 표시 합니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 계정 추가
```
PS C:\> Add-AzureAccount
```

이 명령은 Windows PowerShell에 Azure 계정을 추가 합니다.
명령을 실행 하면 windows에서 계정의 사용자 이름 및 암호를 요청 하기 위해 팝업을 표시 합니다.

### 예제 2: 대체 구독 데이터 파일 사용
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

이 명령은 **subscriptiondatafile** 매개 변수를 사용 하 여 기본 파일 대신 C:\Testing\SDF.xml 파일에 계정 데이터를 저장 하도록 **-Azureaccount 직접 추가** 합니다.

## 변수

### -Credential
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -환경
Azure 환경을 지정 합니다.

Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.
Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.
자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -테 넌 트
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet에는 입력을 파이프로 지정할 수 없습니다.

## 출력

### 않아야
이 cmdlet은 출력을 반환 하지 않습니다.

## 상속자
* **추가-AzureAccount** (및 Azure AD 인증 방법)는 **AzurePublishSettings** (및 관리 인증서 방법) 보다 우선 합니다. 계정에서 **추가-AzureAccount** 를 사용 하는 경우 Azure AD 인증 방법이 사용 되 고 관리 인증서는 무시 됩니다. Azure AD 토큰을 제거 하 고 관리 인증서 메서드를 복원 하려면 **제거-AzureAccount** cmdlet을 사용 합니다. 자세한 내용은 **Get-help 제거-AzureAccount** 를 입력 하세요.
* "귀하의 자격 증명이 만료 되었습니다. Add-AzureAccount을 (를) 사용 하 여 다시 로그인 하십시오. " 액세스 토큰이 만료 되 고 Windows PowerShell에서 Azure 계정에 액세스할 수 없음을 나타냅니다. 계정에 대 한 액세스를 복원 하려면 **-Azureaccount 추가** 를 다시 실행 합니다.
* Azure PowerShell 계정 및 구독 cmdlet은 live Azure 계정이 아닌 구독 데이터 파일에서 데이터를 가져옵니다. Azure 관리 포털을 사용 하는 등 Windows PowerShell 외부에서 계정 또는 구독을 변경 하는 경우 **-AzureAccount** 를 다시 실행 하 여 구독 데이터 파일을 새로 고칩니다.

## 관련 링크

[-AzureEnvironment 추가](./Add-AzureEnvironment.md)

[가져오기-AzureEnvironment](./Get-AzureEnvironment.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[-AzureAccount 제거](./Remove-AzureAccount.md)


