---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServiceEnvironment.md
ms.openlocfilehash: 9641c55dd25d8f09d1898bdda37fafa840db0a19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983899"
---
# <span data-ttu-id="939d3-101">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="939d3-101">Get-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="939d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="939d3-102">SYNOPSIS</span></span>
<span data-ttu-id="939d3-103">App Service Environment를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-103">Gets App Service Environment.</span></span> <span data-ttu-id="939d3-104">리소스 그룹만 지정하면 리소스 그룹에서 ASE 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-104">If only Resource Group is specified, it will return a list of ASE in the Resource Group.</span></span>

## <span data-ttu-id="939d3-105">구문</span><span class="sxs-lookup"><span data-stu-id="939d3-105">SYNTAX</span></span>

```
Get-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="939d3-106">설명</span><span class="sxs-lookup"><span data-stu-id="939d3-106">DESCRIPTION</span></span>
<span data-ttu-id="939d3-107">**Get-AzAppServiceEnvironment** cmdlet은 쿼리와 일치하는 ASE를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-107">The **Get-AzAppServiceEnvironment** cmdlet return ASE(s) matching the query.</span></span>

## <span data-ttu-id="939d3-108">예제</span><span class="sxs-lookup"><span data-stu-id="939d3-108">EXAMPLES</span></span>

### <span data-ttu-id="939d3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="939d3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="939d3-110">에서 명명된 특정 App Service <MyAseName> Environment를 반환합니다. <MyResourceGroup></span><span class="sxs-lookup"><span data-stu-id="939d3-110">Returns a specific App Service Environment named <MyAseName> in <MyResourceGroup></span></span>

## <span data-ttu-id="939d3-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="939d3-111">PARAMETERS</span></span>

### <span data-ttu-id="939d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939d3-112">-DefaultProfile</span></span>
<span data-ttu-id="939d3-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="939d3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="939d3-114">-Name</span></span>
<span data-ttu-id="939d3-115">앱 서비스 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-115">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939d3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="939d3-116">-ResourceGroupName</span></span>
<span data-ttu-id="939d3-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939d3-118">-확인</span><span class="sxs-lookup"><span data-stu-id="939d3-118">-Confirm</span></span>
<span data-ttu-id="939d3-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="939d3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="939d3-120">-WhatIf</span></span>
<span data-ttu-id="939d3-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="939d3-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="939d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939d3-123">CommonParameters</span></span>
<span data-ttu-id="939d3-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="939d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939d3-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="939d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939d3-126">입력</span><span class="sxs-lookup"><span data-stu-id="939d3-126">INPUTS</span></span>

### <span data-ttu-id="939d3-127">없음</span><span class="sxs-lookup"><span data-stu-id="939d3-127">None</span></span>

## <span data-ttu-id="939d3-128">출력</span><span class="sxs-lookup"><span data-stu-id="939d3-128">OUTPUTS</span></span>

### <span data-ttu-id="939d3-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="939d3-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment</span></span>

## <span data-ttu-id="939d3-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="939d3-130">NOTES</span></span>

## <span data-ttu-id="939d3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="939d3-131">RELATED LINKS</span></span>

[<span data-ttu-id="939d3-132">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="939d3-132">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="939d3-133">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="939d3-133">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="939d3-134">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="939d3-134">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)