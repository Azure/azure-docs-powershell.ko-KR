---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e3f246a77d4adb489f660a56d3843520d3a327ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877132"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
가상 컴퓨터에 대 한 SSH 공개 키를 추가 합니다.

## 구문과

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVMSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통해 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.

## 예제의

### 예제 1: 가상 컴퓨터에 공개 키 추가
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

첫 번째 명령은 **AzVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.
명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.

두 번째 명령은 Path 매개 변수에서 지정 하는 VirtualMachine07의 위치에 공개 키를 추가 합니다.

## 변수

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

### -KeyData
공개 키의 기본 64 인코딩을 지정 합니다.
SSH를 사용 하거나이 매개 변수에서 지정 하는 키를 사용 하 여 가상 컴퓨터에 연결할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.
파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.
[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualMachine
' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.

## 출력

### PSVirtualMachine를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[새로운 AzVMConfig](./New-AzVMConfig.md)
