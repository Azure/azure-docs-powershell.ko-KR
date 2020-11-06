---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526435"
---
# Remove-AzureStorageDirectory

## SYNOPSIS
디렉터리를 삭제 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ShareName (기본값)
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 공유
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 디렉토리로
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**제거-AzureStorageDirectory** cmdlet은 디렉터리를 삭제 합니다.

## 예제의

### 예제 1: 폴더 삭제
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoWorkingFolder 이라는 폴더를 삭제 합니다.

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
저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -디렉터리
폴더를 **Cloudfiledirectory** 개체로 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 폴더를 제거 합니다.
디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.
**Get-AzureStorageFile** cmdlet을 사용 하 여 디렉터리를 가져올 수도 있습니다.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
이 cmdlet이 성공한 경우 $True 값을 반환 함을 나타냅니다.
이 매개 변수를 지정 하 고 _Path_ 매개 변수에 적절 하지 않은 값으로 인해 cmdlet이 실패 하는 경우 cmdlet은 오류를 반환 합니다.
이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.

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

### -Path
폴더의 경로를 지정 합니다.
이 매개 변수가 지정 하는 폴더가 비어 있으면이 cmdlet은 해당 폴더를 삭제 합니다.
폴더가 비어 있지 않은 경우이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
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

### -공유
**Cloudfileshare** 되지 않는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.
**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.
이 개체는 저장소 컨텍스트를 포함 합니다.
이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
파일 공유의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure 파일. c a c 공유
매개 변수: Share (ByValue)

### WindowsAzure. c l i 파일 디렉터리
매개 변수: Directory (ByValue)

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. c l i 파일 디렉터리

## 상속자

## 관련 링크

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)

[새-AzureStorageDirectory](./New-AzureStorageDirectory.md)
