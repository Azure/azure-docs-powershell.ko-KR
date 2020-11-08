---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046352"
---
# Get-AzureEnvironment

## SYNOPSIS
Azure 환경을 가져옵니다.

## 구문과

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get AzureEnvironment** Cmdlet은 Windows PowerShell에서 사용할 수 있는 Azure 환경을 가져옵니다.

Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.
Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.
자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

**Get-AzureEnvironment** Cmdlet은 Azure가 아닌 구독 데이터 파일에서 환경을 가져옵니다.
구독 데이터 파일이 오래 된 경우 **추가-AzureAccount** 또는 **import-module settingsfile** cmdlet을 실행 하 여 새로 고칩니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 모든 환경 가져오기
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

이 명령은 Windows PowerShell에서 사용할 수 있는 모든 환경을 가져옵니다.

### 예제 2: 이름으로 환경 가져오기
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

이 예제에서는 AzureCloud 환경을 가져옵니다.

### 예제 3: 모든 환경의 모든 속성 가져오기
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

이 명령은 모든 환경의 모든 속성을 가져옵니다.

이 명령은 **Get AzureEnvironment** cmdlet을 사용 하 여이 계정에 대 한 모든 Azure 환경을 가져옵니다.
그런 다음 **Foreach-개체** cmdlet을 사용 하 여 각 환경의 **Name** 매개 변수를 사용 하 여 **Get-azureenvironment** 명령을 실행 합니다.
**Name** 매개 변수 값은 각 환경의 environment **이름** 속성입니다.

**Get-AzureEnvironment** 는 매개 변수 없이 환경의 선택 된 속성만 가져옵니다.

## 변수

### -이름
지정 된 환경만 가져옵니다.
환경 이름을 입력 합니다.
매개 변수 값은 대/소문자를 구분 합니다.
와일드 카드 문자는 허용 되지 않습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### PSCustomObject (Management)
기본적으로 **Get-AzureEnvironment** 는 사용자 지정 개체를 반환 합니다.

### WindowsAzure. 유틸리티. 공용 WindowsAzureEnvironment
**Name** 매개 변수를 사용 하 여 **가져오기-azureenvironment** 를 실행 하는 경우 **windowsazureenvironment** 개체를 반환 합니다.

## 상속자

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[-AzureEnvironment 추가](./Add-AzureEnvironment.md)

[Get-Azure도움말 파일](./Get-AzurePublishSettingsFile.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)

[-AzureEnvironment 제거](./Remove-AzureEnvironment.md)

[Set AzureEnvironment](./Set-AzureEnvironment.md)


