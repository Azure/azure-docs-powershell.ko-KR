---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204225"
---
# Set-AzStorageContainerAcl

## SYNOPSIS
저장소 컨테이너에 대 한 공용 액세스 권한을 설정 합니다.

## 구문과

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 설명은
**Set-AzStorageContainerAcl** Cmdlet은 Azure의 지정 된 저장소 컨테이너에 대 한 공용 액세스 권한을 설정 합니다.

## 예제의

### 예제 1: 이름별로 azure storage 컨테이너 ACL 설정
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

이 명령은 공용 액세스 권한이 없는 컨테이너를 만듭니다.

### 예제 2: 파이프라인을 사용 하 여 azure storage 컨테이너 ACL 설정
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

이 명령은 이름이 컨테이너로 시작 하는 모든 저장소 컨테이너를 가져온 다음 파이프라인에 해당 결과를 전달 하 여 해당 파일에 대 한 권한을 모두 Blob 액세스로 설정 합니다.

## 변수

### -ClientTimeoutPerRequest
한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.
이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.
이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

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
New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
컨테이너 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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

### -사용 권한
이 컨테이너에 대 한 공용 액세스 수준을 지정 합니다.
기본적으로 컨테이너 및 그 안의 모든 blob에는 저장소 계정의 소유자만 액세스할 수 있습니다.
컨테이너 및 해당 blob에 대 한 읽기 권한을 익명 사용자에 게 부여 하려면 공용 액세스를 사용 하도록 컨테이너 사용 권한을 설정할 수 있습니다.
익명 사용자는 요청을 인증 하지 않고 공개적으로 사용할 수 있는 컨테이너에서 blob을 읽을 수 있습니다.
이 매개 변수에 허용 되는 값은--컨테이너입니다.
컨테이너 및 해당 blob에 대 한 전체 읽기 액세스를 제공 합니다.
클라이언트는 익명 요청을 통해 컨테이너의 blob을 열거할 수 있지만 저장소 계정의 컨테이너를 열거할 수 없습니다. --Blob.
익명 요청을 통해 컨테이너의 blob 데이터에 대 한 읽기 액세스를 제공 하지만 컨테이너 데이터에 대 한 액세스는 제공 하지 않습니다.
클라이언트는 익명 요청을 사용 하 여 컨테이너의 blob을 열거할 수 없습니다. --Off.
저장소 계정 소유자만 액세스를 제한 합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.
서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.
각 요청에 대 한 서버 쪽 시간이 초과 되었습니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.

## 상속자

## 관련 링크

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[새로운 AzStorageContainer](./New-AzStorageContainer.md)

[제거-AzStorageContainer](./Remove-AzStorageContainer.md)


