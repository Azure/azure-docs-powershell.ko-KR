---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368901"
---
# <span data-ttu-id="9e811-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9e811-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="9e811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e811-102">SYNOPSIS</span></span>
<span data-ttu-id="9e811-103">VM 확장 집합에 있는 VM의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="9e811-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e811-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e811-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e811-105">DESCRIPTION</span></span>
<span data-ttu-id="9e811-106">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="9e811-107">예제</span><span class="sxs-lookup"><span data-stu-id="9e811-107">EXAMPLES</span></span>

### <span data-ttu-id="9e811-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e811-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="9e811-109">Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VM 확장 집합에서 VM 인스턴스 1의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="9e811-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e811-110">PARAMETERS</span></span>

### <span data-ttu-id="9e811-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e811-111">-DefaultProfile</span></span>
<span data-ttu-id="9e811-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e811-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="9e811-113">-ExtensionName</span></span>
<span data-ttu-id="9e811-114">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-114">The extension name.</span></span>
<span data-ttu-id="9e811-115">이 매개 변수를 지정하지 않으면 사용되는 기본값은 Windows VM용 AzureDiskEncryption 및 Linux VM용 AzureDiskEncryptionForLinux입니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="9e811-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9e811-116">-InstanceId</span></span>
<span data-ttu-id="9e811-117">인스턴스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="9e811-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e811-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e811-119">가상 머신 확장 집합의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9e811-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9e811-120">-VMScaleSetName</span></span>
<span data-ttu-id="9e811-121">가상 머신 확장 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="9e811-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e811-122">CommonParameters</span></span>
<span data-ttu-id="9e811-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e811-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e811-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e811-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e811-125">입력</span><span class="sxs-lookup"><span data-stu-id="9e811-125">INPUTS</span></span>

### <span data-ttu-id="9e811-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9e811-126">System.String</span></span>

## <span data-ttu-id="9e811-127">출력</span><span class="sxs-lookup"><span data-stu-id="9e811-127">OUTPUTS</span></span>

### <span data-ttu-id="9e811-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="9e811-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="9e811-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e811-129">NOTES</span></span>

## <span data-ttu-id="9e811-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e811-130">RELATED LINKS</span></span>
