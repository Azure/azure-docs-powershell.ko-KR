---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045950"
---
# Set-AzureSubscription

## SYNOPSIS
Azure 구독을 변경 합니다.

## 구문과

### UpdateSubscriptionByIdParameterSetName (기본값)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Set-AzureSubscription** Cmdlet은 Azure 구독 개체의 속성을 설정 하 고 변경 합니다.
이 cmdlet을 사용 하 여 기본 구독이 아닌 Azure 구독에서 작동 하거나 현재 저장소 계정을 변경할 수 있습니다.
현재 및 기본 구독에 대 한 자세한 내용은 **Select-AzureSubscription** cmdlet을 참조 하세요.

이 cmdlet은 실제 Azure 구독이 아닌 Azure 구독 개체에서 작동 합니다.
Azure 구독을 만들고 프로 비전 하려면 [Azure 포털](https://azure.microsoft.com/) ()을 방문 하세요 https://azure.microsoft.com/) .

이 cmdlet은 Windows PowerShell에 Azure 계정을 추가 하는 데 **-AzureAccount** 또는 **Import-Azureaccount settingsfile** cmdlet을 사용할 때 생성 하는 구독 데이터 파일의 데이터를 변경 합니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 기존 subscription1 변경
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

이 예제에서는 ContosoEngineering 이라는 구독에 대 한 인증서를 변경 합니다.

### 예제 2: 서비스 끝점 변경
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

이 명령은 ContosoEngineering 구독에 대 한 사용자 지정 서비스 끝점을 추가 하거나 변경 합니다.

### 예제 3: 속성 값 지우기
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

이 명령은 인증서 및 ResourceManagerEndpoint 속성의 값을 null ($Null)로 설정 합니다.
이렇게 하면 다른 설정을 변경 하지 않고 해당 속성의 값이 지워집니다.

### 예제 4: 대체 구독 데이터 파일 사용
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

이 명령은 ContosoFinance 구독의 현재 저장소 계정을 ContosoStorage01으로 변경 합니다.
이 명령은 **subscriptiondatafile** 파일 매개 변수를 사용 하 여 C:\Azure\SubscriptionData.xml subscription data 파일의 데이터를 변경 합니다.
기본적으로 **Set-AzureSubscription** 는 로밍 사용자 프로필의 기본 구독 데이터 파일을 사용 합니다.

## 변수

### -인증서
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -컨텍스트
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
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

### -PassThru
명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.
기본적으로이 cmdlet은 출력을 반환 하지 않습니다.
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

### -ResourceManagerEndpoint
계정과 연결 된 리소스 그룹에 대 한 데이터를 포함 하 여 Azure Resource Manager 데이터에 대 한 끝점을 지정 합니다.
Azure 리소스 관리자에 대 한 자세한 내용은 [Azure Resource Manager cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) 및 [Windows PowerShell을 사용 하 여 리소스 관리자](https://go.microsoft.com/fwlink/?LinkID=394767)  ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionId
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### 없음 또는 시스템 부울
*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.
기본적으로이 cmdlet은 출력을 반환 하지 않습니다.

## 상속자

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)

[제거-AzureSubscription](./Remove-AzureSubscription.md)

[선택-AzureSubscription](./Select-AzureSubscription.md)


