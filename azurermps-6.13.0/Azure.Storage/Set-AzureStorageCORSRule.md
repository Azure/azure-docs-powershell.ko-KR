---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
ms.openlocfilehash: 21293b8262a10c5710ed132413658c3c1cfbd254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526428"
---
# Set-AzureStorageCORSRule

## SYNOPSIS
저장소 서비스 유형에 대 한 CORS 규칙을 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명은
**AzureStorageCORSRule** Cmdlet은 Azure 저장소 서비스 유형에 대 한 CORS (교차 원본 리소스 공유) 규칙을 설정 합니다.
이 cmdlet에 대 한 저장소 서비스의 유형은 Blob, 테이블, 큐 및 파일입니다.
이 cmdlet은 기존 규칙을 덮어씁니다.
현재 규칙을 보려면 Get-AzureStorageCORSRule cmdlet을 사용 합니다.

## 예제의

### 예제 1: blob 서비스에 CORS 규칙 할당
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

첫 번째 명령은 $CorsRules 변수에 규칙 배열을 할당 합니다.
이 명령은이 코드 블록의 여러 줄에 걸쳐 표준 확장을 사용 합니다.
두 번째 명령은 $CorsRules의 규칙을 Blob 서비스 유형에 할당 합니다.

### 예제 2: blob 서비스에 대 한 CORS 규칙의 속성 변경
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

첫 번째 명령은 **AzureStorageCORSRule** cmdlet을 사용 하 여 Blob 형식에 대 한 현재 CORS 규칙을 가져옵니다.
명령은 $CorsRules 배열 변수에 규칙을 저장 합니다.
두 번째 및 세 번째 명령은 $CorsRules의 첫 번째 규칙을 수정 합니다.
마지막 명령은 $CorsRules의 규칙을 Blob 서비스 형식에 할당 합니다.
수정 된 규칙은 현재 CORS 규칙을 덮어씁니다.

## 변수

### -ClientTimeoutPerRequest
한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.
이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.
이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
최대 동시 네트워크 통화를 지정 합니다.
이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.
지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.
이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
기본값은 10입니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -CorsRules
CORS 규칙의 배열을 지정 합니다.
Get-AzureStorageCORSRule cmdlet을 사용 하 여 기존 규칙을 검색할 수 있습니다.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 작업의 성공 여부를 반영 하는 Boolean을 반환 함을 나타냅니다.
기본적으로이 cmdlet은 값을 반환 하지 않습니다.

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

### -ServerTimeoutPerRequest
요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
이 cmdlet이 규칙을 할당 하는 Azure 저장소 서비스 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 블 
- 테이블로 
- 전담팀 
- 파일

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 PSCorsRule로 저장 합니다.

## 상속자

## 관련 링크

[Get-AzureStorageCORSRule](./Get-AzureStorageCORSRule.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)

[제거-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)


