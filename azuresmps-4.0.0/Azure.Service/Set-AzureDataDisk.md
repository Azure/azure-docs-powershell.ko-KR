---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046066"
---
# Set-AzureDataDisk

## SYNOPSIS
Azure 가상 머신에서 기존 데이터 디스크의 호스트 캐싱을 수정 합니다.

## 구문과

### 로이 Esize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 길이
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**Set AzureDataDisk** Cmdlet은 Azure 가상 머신에서 기존 데이터 디스크의 캐시 특성을 수정 합니다.
LUN (논리 단위 번호)을 기준으로 업데이트할 데이터 디스크를 지정 합니다.

## 예제의

### 예제 1: 데이터 디스크에 대 한 호스트 캐싱 수정
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

이 명령은 **get-help** cmdlet을 사용 하 여 ContosoService 이라는 서비스에서 실행 되는 가상 컴퓨터를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.
해당 cmdlet은 VirtualMachine07 이라는 가상 컴퓨터의 LUN 2에 데이터 디스크를 설정 하 여 읽기 전용 호스트 캐싱을 사용 합니다.
이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

### 예제 2: 가상 컴퓨터의 모든 데이터 디스크에 대 한 호스트 캐싱 수정
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

이 명령은 ContosoService 클라우드 서비스의 VirtualMachine07 이라는 가상 컴퓨터에 대 한 개체를 가져옵니다.
명령이 해당 가상 컴퓨터에 대 한 데이터 디스크를 가져오는 **AzureDataDisk** cmdlet에이를 전달 합니다.
그런 다음 현재 cmdlet은 각 데이터 디스크의 호스트 캐싱 모드를 ReadWrite로 설정 합니다.
이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

## 변수

### -DiskName
이 cmdlet이 수정 하는 데이터 디스크 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> 디스크 캐시는 4 TiB 이상에서 지원 되지 않습니다. VM에 여러 개의 디스크가 연결 된 경우 4 TiB 보다 작은 각 디스크는 캐싱을 지원 합니다.
>
> Azure 디스크의 캐시 설정을 변경 하면 대상 디스크가 분리 되 고 다시 연결 됩니다. 운영 체제 디스크인 경우 VM이 다시 시작 됩니다. 디스크 캐시 설정을 변경 하기 전에이 중단에 영향을 받을 수 있는 모든 응용 프로그램/서비스를 중지 합니다. 이러한 권장 사항을 팔 로우 하지 않으면 데이터 손상이 발생할 수 있습니다.

디스크의 호스트 수준 캐싱 설정을 지정 합니다.
유효한 값은 다음과 같습니다.

- 않아야
- 읽기
- 쓰기

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LUN
가상 컴퓨터의 데이터 드라이브에 대 한 LUN을 지정 합니다.
유효한 값은 0 ~ 15입니다.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -ResizedSizeInGB
데이터 디스크의 새 크기 (기가바이트)를 지정 합니다.
새 크기는 현재 크기 보다 커야 합니다.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
데이터 디스크에 연결 된 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[-AzureDataDisk 추가](./Add-AzureDataDisk.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[-AzureDataDisk 제거](./Remove-AzureDataDisk.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


