---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045735"
---
# Add-AzureDataDisk

## SYNOPSIS
가상 컴퓨터에 데이터 디스크를 추가 합니다.

## 구문과

### CreateNew (기본값)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Import
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### 가져오기 원본
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**추가-AzureDataDisk** cmdlet은 새 또는 기존 데이터 디스크를 Azure 가상 컴퓨터 개체에 추가 합니다.
*CreateNew* 매개 변수를 사용 하 여 지정 된 크기 및 레이블을 갖는 새 데이터 디스크를 만듭니다.
*Import* 매개 변수를 사용 하 여 이미지 리포지토리의 기존 디스크를 연결 합니다.
*가져오기* 매개 변수를 사용 하 여 저장소 계정의 blob에서 기존 디스크를 연결 합니다.
연결 된 데이터 디스크의 호스트 캐시 모드를 지정할 수 있습니다.

## 예제의

### 예제 1: 리포지토리에서 데이터 디스크 가져오기
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

이 명령은 **VirtualMachine07 cmdlet을** 사용 하 여 ContosoService cloud 서비스의 가상 컴퓨터 이름에 대 한 가상 컴퓨터 개체를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.
이 명령은 저장소의 기존 데이터 디스크를 가상 컴퓨터에 연결 합니다.
데이터 디스크의 LUN은 0입니다.
이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

### 예제 2: 새 데이터 디스크 추가
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

이 명령은 VirtualMachine08 이라는 가상 컴퓨터에 대 한 가상 컴퓨터 개체를 가져옵니다.
명령이 현재 cmdlet에이를 전달 합니다.
이 명령은 MyNewDisk 이라는 새 데이터 디스크를 연결 합니다.
Cmdlet은 현재 구독에 대 한 기본 저장소 계정의 vhd 컨테이너에 디스크를 만듭니다.
이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

### 예제 3: 지정 된 위치에서 데이터 디스크 추가
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

이 명령은 가상 머신 데이터베이스에 대 한 가상 머신 개체를 가져옵니다.
명령이 현재 cmdlet에이를 전달 합니다.
이 명령은 지정 된 위치에서 Disk14 라는 기존 데이터 디스크를 연결 합니다.
이 명령은 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.

## 변수

### -CreateNew
이 cmdlet이 데이터 디스크를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
새 데이터 디스크에 대 한 디스크 레이블을 지정 합니다.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
디스크 리포지토리의 데이터 디스크 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
새 데이터 디스크에 대 한 논리 디스크 크기 (기가바이트)를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
디스크의 호스트 수준 캐싱 설정을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 않아야 
- 읽기 
- 쓰기

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

### -가져오기
이 cmdlet이 이미지 리포지토리에서 기존 데이터 디스크를 가져오도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
이 cmdlet이 저장소 계정의 blob에서 기존 데이터 디스크를 가져오도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
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
가상 컴퓨터의 데이터 드라이브에 대 한 LUN (논리 단위 번호)을 지정 합니다.
유효한 값은 0 ~ 15입니다.
각 데이터 디스크에는 고유한 LUN이 있어야 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
이 cmdlet이 데이터 디스크를 저장 하는 Azure storage 계정에서 blob의 위치를 지정 합니다.
위치를 지정 하지 않으면 cmdlet은 현재 구독에 대 한 기본 저장소 계정의 데이터 디스크를 vhd 컨테이너에 저장 합니다.
Vhd 컨테이너가 없는 경우 cmdlet은 vhd 컨테이너를 만듭니다.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -VM
이 cmdlet이 데이터 디스크를 연결 하는 가상 컴퓨터 개체를 지정 합니다.
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

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[-AzureDataDisk 제거](./Remove-AzureDataDisk.md)

[Set AzureDataDisk](./Set-AzureDataDisk.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


