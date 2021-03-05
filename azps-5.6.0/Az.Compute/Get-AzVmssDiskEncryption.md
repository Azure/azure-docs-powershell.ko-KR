---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 56fcbadbcdbd874df3fea74918381eb24b2fa1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980907"
---
# <span data-ttu-id="0f0f5-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0f0f5-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="0f0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0f5-103">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="0f0f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f0f5-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="0f0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0f5-106">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="0f0f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="0f0f5-107">EXAMPLES</span></span>

### <span data-ttu-id="0f0f5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f0f5-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0f0f5-109">Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0f0f5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f0f5-110">PARAMETERS</span></span>

### <span data-ttu-id="0f0f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0f5-111">-DefaultProfile</span></span>
<span data-ttu-id="0f0f5-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0f5-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0f0f5-113">-ExtensionName</span></span>
<span data-ttu-id="0f0f5-114">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-114">The extension name.</span></span>
<span data-ttu-id="0f0f5-115">이 매개 변수를 지정하지 않으면 Windows VM에 대한 AzureDiskEncryption 및 Linux VM용 AzureDiskEncryptionForLinux가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="0f0f5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0f5-116">-ResourceGroupName</span></span>
<span data-ttu-id="0f0f5-117">가상 머신 확장 집합의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0f0f5-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f5-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0f0f5-118">-VMScaleSetName</span></span>
<span data-ttu-id="0f0f5-119">가상 머신 확장 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0f5-120">CommonParameters</span></span>
<span data-ttu-id="0f0f5-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0f5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0f5-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f0f5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0f5-123">입력</span><span class="sxs-lookup"><span data-stu-id="0f0f5-123">INPUTS</span></span>

### <span data-ttu-id="0f0f5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0f0f5-124">System.String</span></span>

## <span data-ttu-id="0f0f5-125">출력</span><span class="sxs-lookup"><span data-stu-id="0f0f5-125">OUTPUTS</span></span>

### <span data-ttu-id="0f0f5-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="0f0f5-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="0f0f5-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f0f5-127">NOTES</span></span>

## <span data-ttu-id="0f0f5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f0f5-128">RELATED LINKS</span></span>
