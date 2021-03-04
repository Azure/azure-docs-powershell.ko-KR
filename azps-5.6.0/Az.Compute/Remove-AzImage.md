---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: bcbfaefcc94415acdd1100025e1eefc2977f107a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954848"
---
# <span data-ttu-id="7a624-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="7a624-101">Remove-AzImage</span></span>

## <span data-ttu-id="7a624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a624-102">SYNOPSIS</span></span>
<span data-ttu-id="7a624-103">이미지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-103">Removes an image.</span></span>

## <span data-ttu-id="7a624-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a624-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a624-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a624-105">DESCRIPTION</span></span>
<span data-ttu-id="7a624-106">**Remove-AzImage** cmdlet은 이미지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="7a624-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a624-107">EXAMPLES</span></span>

### <span data-ttu-id="7a624-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a624-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="7a624-109">이 명령은 리소스 그룹 'ResourceGroup01'에서 'Image01'이라는 이미지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7a624-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a624-110">PARAMETERS</span></span>

### <span data-ttu-id="7a624-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a624-111">-AsJob</span></span>
<span data-ttu-id="7a624-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7a624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a624-113">-DefaultProfile</span></span>
<span data-ttu-id="7a624-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a624-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a624-115">-Force</span></span>
<span data-ttu-id="7a624-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a624-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7a624-117">-ImageName</span></span>
<span data-ttu-id="7a624-118">이미지의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7a624-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a624-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a624-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a624-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7a624-121">-Confirm</span></span>
<span data-ttu-id="7a624-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a624-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a624-123">-WhatIf</span></span>
<span data-ttu-id="7a624-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a624-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a624-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a624-126">CommonParameters</span></span>
<span data-ttu-id="7a624-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a624-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a624-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a624-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a624-129">입력</span><span class="sxs-lookup"><span data-stu-id="7a624-129">INPUTS</span></span>

### <span data-ttu-id="7a624-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7a624-130">System.String</span></span>

## <span data-ttu-id="7a624-131">출력</span><span class="sxs-lookup"><span data-stu-id="7a624-131">OUTPUTS</span></span>

### <span data-ttu-id="7a624-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7a624-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7a624-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a624-133">NOTES</span></span>

## <span data-ttu-id="7a624-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a624-134">RELATED LINKS</span></span>
