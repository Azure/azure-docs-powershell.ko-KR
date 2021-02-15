---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204053"
---
# <span data-ttu-id="1dcf5-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="1dcf5-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="1dcf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcf5-103">Front Door에서 콘텐츠 제거</span><span class="sxs-lookup"><span data-stu-id="1dcf5-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="1dcf5-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dcf5-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dcf5-105">설명</span><span class="sxs-lookup"><span data-stu-id="1dcf5-105">DESCRIPTION</span></span>
<span data-ttu-id="1dcf5-106">Remove-AzFrontDoorContent Front Door에서 캐시된 콘텐츠를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="1dcf5-107">예제</span><span class="sxs-lookup"><span data-stu-id="1dcf5-107">EXAMPLES</span></span>

### <span data-ttu-id="1dcf5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dcf5-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="1dcf5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dcf5-109">PARAMETERS</span></span>

### <span data-ttu-id="1dcf5-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="1dcf5-110">-ContentPath</span></span>
<span data-ttu-id="1dcf5-111">제거될 콘텐츠의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcf5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcf5-112">-DefaultProfile</span></span>
<span data-ttu-id="1dcf5-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dcf5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1dcf5-114">-Name</span></span>
<span data-ttu-id="1dcf5-115">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcf5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dcf5-116">-PassThru</span></span>
<span data-ttu-id="1dcf5-117">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="1dcf5-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="1dcf5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dcf5-118">-ResourceGroupName</span></span>
<span data-ttu-id="1dcf5-119">Front Door의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1dcf5-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dcf5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dcf5-120">-Confirm</span></span>
<span data-ttu-id="1dcf5-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dcf5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dcf5-122">-WhatIf</span></span>
<span data-ttu-id="1dcf5-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1dcf5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dcf5-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dcf5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcf5-125">CommonParameters</span></span>
<span data-ttu-id="1dcf5-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcf5-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dcf5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcf5-128">입력</span><span class="sxs-lookup"><span data-stu-id="1dcf5-128">INPUTS</span></span>

### <span data-ttu-id="1dcf5-129">없음</span><span class="sxs-lookup"><span data-stu-id="1dcf5-129">None</span></span>

## <span data-ttu-id="1dcf5-130">출력</span><span class="sxs-lookup"><span data-stu-id="1dcf5-130">OUTPUTS</span></span>

### <span data-ttu-id="1dcf5-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1dcf5-131">System.Boolean</span></span>

## <span data-ttu-id="1dcf5-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dcf5-132">NOTES</span></span>

## <span data-ttu-id="1dcf5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dcf5-133">RELATED LINKS</span></span>
