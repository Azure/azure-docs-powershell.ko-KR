---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994485"
---
# <span data-ttu-id="65bbb-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="65bbb-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="65bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="65bbb-103">VM 확장 집합에서 VM의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="65bbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="65bbb-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65bbb-105">설명</span><span class="sxs-lookup"><span data-stu-id="65bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="65bbb-106">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="65bbb-107">예제</span><span class="sxs-lookup"><span data-stu-id="65bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="65bbb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="65bbb-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="65bbb-109">Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VM 확장 집합에서 VM 인스턴스 1의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="65bbb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="65bbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bbb-111">-DefaultProfile</span></span>
<span data-ttu-id="65bbb-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65bbb-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="65bbb-113">-ExtensionName</span></span>
<span data-ttu-id="65bbb-114">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-114">The extension name.</span></span>
<span data-ttu-id="65bbb-115">이 매개 변수를 지정하지 않으면 Windows VM에 대한 AzureDiskEncryption 및 Linux VM용 AzureDiskEncryptionForLinux가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="65bbb-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="65bbb-116">-InstanceId</span></span>
<span data-ttu-id="65bbb-117">인스턴스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="65bbb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65bbb-118">-ResourceGroupName</span></span>
<span data-ttu-id="65bbb-119">가상 머신 확장 집합의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="65bbb-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65bbb-120">-VMScaleSetName</span></span>
<span data-ttu-id="65bbb-121">가상 머신 확장 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="65bbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bbb-122">CommonParameters</span></span>
<span data-ttu-id="65bbb-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65bbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bbb-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65bbb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bbb-125">입력</span><span class="sxs-lookup"><span data-stu-id="65bbb-125">INPUTS</span></span>

### <span data-ttu-id="65bbb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="65bbb-126">System.String</span></span>

## <span data-ttu-id="65bbb-127">출력</span><span class="sxs-lookup"><span data-stu-id="65bbb-127">OUTPUTS</span></span>

### <span data-ttu-id="65bbb-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="65bbb-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="65bbb-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65bbb-129">NOTES</span></span>

## <span data-ttu-id="65bbb-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65bbb-130">RELATED LINKS</span></span>
