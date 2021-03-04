---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: f73569e8e40af5111a738496ba6ad41ff03058f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969451"
---
# <span data-ttu-id="496bd-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="496bd-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="496bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496bd-102">SYNOPSIS</span></span>
<span data-ttu-id="496bd-103">Blob 기반 디스크가 있는 가상 머신을 관리 디스크가 있는 가상 머신으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="496bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="496bd-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="496bd-105">설명</span><span class="sxs-lookup"><span data-stu-id="496bd-105">DESCRIPTION</span></span>
<span data-ttu-id="496bd-106">**ConvertTo-AzVMManagedDisk** cmdlet은 Blob 기반 디스크가 있는 가상 머신을 관리 디스크가 있는 가상 머신으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="496bd-107">이 작업을 호출하기 전에 가상 머신을 중지 취소해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="496bd-108">예제</span><span class="sxs-lookup"><span data-stu-id="496bd-108">EXAMPLES</span></span>

### <span data-ttu-id="496bd-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="496bd-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="496bd-110">이 명령은 리소스 그룹 'ResourceGroup01'의 'VM01'이라는 가상 머신의 Blob 기반 디스크를 관리 디스크로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="496bd-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="496bd-111">PARAMETERS</span></span>

### <span data-ttu-id="496bd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="496bd-112">-AsJob</span></span>
<span data-ttu-id="496bd-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="496bd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="496bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496bd-114">-DefaultProfile</span></span>
<span data-ttu-id="496bd-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="496bd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496bd-116">-ResourceGroupName</span></span>
<span data-ttu-id="496bd-117">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="496bd-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="496bd-118">-VMName</span></span>
<span data-ttu-id="496bd-119">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="496bd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="496bd-120">-Confirm</span></span>
<span data-ttu-id="496bd-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496bd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496bd-122">-WhatIf</span></span>
<span data-ttu-id="496bd-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="496bd-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496bd-125">CommonParameters</span></span>
<span data-ttu-id="496bd-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="496bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496bd-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="496bd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496bd-128">입력</span><span class="sxs-lookup"><span data-stu-id="496bd-128">INPUTS</span></span>

### <span data-ttu-id="496bd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="496bd-129">System.String</span></span>

## <span data-ttu-id="496bd-130">출력</span><span class="sxs-lookup"><span data-stu-id="496bd-130">OUTPUTS</span></span>

### <span data-ttu-id="496bd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="496bd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="496bd-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="496bd-132">NOTES</span></span>

## <span data-ttu-id="496bd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="496bd-133">RELATED LINKS</span></span>
