---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364197"
---
# <span data-ttu-id="11545-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="11545-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="11545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11545-102">SYNOPSIS</span></span>
<span data-ttu-id="11545-103">Blob 기반 디스크가 있는 가상 머신을 관리 디스크가 있는 가상 머신으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="11545-104">구문</span><span class="sxs-lookup"><span data-stu-id="11545-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11545-105">설명</span><span class="sxs-lookup"><span data-stu-id="11545-105">DESCRIPTION</span></span>
<span data-ttu-id="11545-106">**ConvertTo-AzVMManagedDisk** cmdlet은 Blob 기반 디스크가 있는 가상 머신을 관리 디스크가 있는 가상 머신으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="11545-107">이 작업을 호출하기 전에 가상 머신을 중지-취소해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="11545-108">예제</span><span class="sxs-lookup"><span data-stu-id="11545-108">EXAMPLES</span></span>

### <span data-ttu-id="11545-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="11545-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="11545-110">이 명령은 리소스 그룹 'ResourceGroup01'의 'VM01'이라는 가상 머신의 Blob 기반 디스크를 관리 디스크로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="11545-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11545-111">PARAMETERS</span></span>

### <span data-ttu-id="11545-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11545-112">-AsJob</span></span>
<span data-ttu-id="11545-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="11545-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11545-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11545-114">-DefaultProfile</span></span>
<span data-ttu-id="11545-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11545-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11545-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11545-116">-ResourceGroupName</span></span>
<span data-ttu-id="11545-117">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="11545-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="11545-118">-VMName</span></span>
<span data-ttu-id="11545-119">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="11545-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11545-120">-Confirm</span></span>
<span data-ttu-id="11545-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11545-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11545-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11545-122">-WhatIf</span></span>
<span data-ttu-id="11545-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="11545-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11545-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11545-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11545-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11545-125">CommonParameters</span></span>
<span data-ttu-id="11545-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11545-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11545-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11545-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11545-128">입력</span><span class="sxs-lookup"><span data-stu-id="11545-128">INPUTS</span></span>

### <span data-ttu-id="11545-129">System.String</span><span class="sxs-lookup"><span data-stu-id="11545-129">System.String</span></span>

## <span data-ttu-id="11545-130">출력</span><span class="sxs-lookup"><span data-stu-id="11545-130">OUTPUTS</span></span>

### <span data-ttu-id="11545-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="11545-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="11545-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11545-132">NOTES</span></span>

## <span data-ttu-id="11545-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11545-133">RELATED LINKS</span></span>
