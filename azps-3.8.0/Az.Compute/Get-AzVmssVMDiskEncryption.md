---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034390"
---
# <span data-ttu-id="8535a-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8535a-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="8535a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8535a-102">SYNOPSIS</span></span>
<span data-ttu-id="8535a-103">VM 단위 집합에서 Vm의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="8535a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8535a-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8535a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8535a-105">DESCRIPTION</span></span>
<span data-ttu-id="8535a-106">VM 확장 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="8535a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8535a-107">EXAMPLES</span></span>

### <span data-ttu-id="8535a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8535a-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="8535a-109">Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VM 크기 집합에서 VM 인스턴스 1의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="8535a-110">변수</span><span class="sxs-lookup"><span data-stu-id="8535a-110">PARAMETERS</span></span>

### <span data-ttu-id="8535a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8535a-111">-DefaultProfile</span></span>
<span data-ttu-id="8535a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535a-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8535a-113">-ExtensionName</span></span>
<span data-ttu-id="8535a-114">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-114">The extension name.</span></span>
<span data-ttu-id="8535a-115">이 매개 변수를 지정 하지 않으면 windows Vm 용 azurediskencryption 용 AzureDiskEncryption를 사용 하 여 기본 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8535a-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8535a-116">-InstanceId</span></span>
<span data-ttu-id="8535a-117">인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-117">Specifies the instance ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8535a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8535a-118">-ResourceGroupName</span></span>
<span data-ttu-id="8535a-119">가상 컴퓨터 크기 집합의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-119">Resource group name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8535a-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8535a-120">-VMScaleSetName</span></span>
<span data-ttu-id="8535a-121">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8535a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8535a-122">CommonParameters</span></span>
<span data-ttu-id="8535a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8535a-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8535a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8535a-125">입력</span><span class="sxs-lookup"><span data-stu-id="8535a-125">INPUTS</span></span>

### <span data-ttu-id="8535a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8535a-126">System.String</span></span>

## <span data-ttu-id="8535a-127">출력</span><span class="sxs-lookup"><span data-stu-id="8535a-127">OUTPUTS</span></span>

### <span data-ttu-id="8535a-128">PSVmssVMDiskEncryptionStatusContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8535a-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="8535a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8535a-129">NOTES</span></span>

## <span data-ttu-id="8535a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8535a-130">RELATED LINKS</span></span>
