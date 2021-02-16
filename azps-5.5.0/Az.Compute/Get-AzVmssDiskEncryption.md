---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204896"
---
# <span data-ttu-id="f5220-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f5220-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="f5220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5220-102">SYNOPSIS</span></span>
<span data-ttu-id="f5220-103">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="f5220-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5220-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5220-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5220-105">DESCRIPTION</span></span>
<span data-ttu-id="f5220-106">VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="f5220-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5220-107">EXAMPLES</span></span>

### <span data-ttu-id="f5220-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5220-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f5220-109">Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VM 확장 집합의 디스크 암호화 상태를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f5220-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5220-110">PARAMETERS</span></span>

### <span data-ttu-id="f5220-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5220-111">-DefaultProfile</span></span>
<span data-ttu-id="f5220-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5220-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f5220-113">-ExtensionName</span></span>
<span data-ttu-id="f5220-114">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-114">The extension name.</span></span>
<span data-ttu-id="f5220-115">이 매개 변수를 지정하지 않으면 사용되는 기본값은 Windows VM의 경우 AzureDiskEncryption, Linux VM의 경우 AzureDiskEncryptionForLinux입니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f5220-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5220-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5220-117">가상 머신 확장 집합의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f5220-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="f5220-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f5220-118">-VMScaleSetName</span></span>
<span data-ttu-id="f5220-119">가상 머신 확장 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="f5220-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5220-120">CommonParameters</span></span>
<span data-ttu-id="f5220-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5220-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5220-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5220-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5220-123">입력</span><span class="sxs-lookup"><span data-stu-id="f5220-123">INPUTS</span></span>

### <span data-ttu-id="f5220-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f5220-124">System.String</span></span>

## <span data-ttu-id="f5220-125">출력</span><span class="sxs-lookup"><span data-stu-id="f5220-125">OUTPUTS</span></span>

### <span data-ttu-id="f5220-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="f5220-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f5220-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5220-127">NOTES</span></span>

## <span data-ttu-id="f5220-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5220-128">RELATED LINKS</span></span>
