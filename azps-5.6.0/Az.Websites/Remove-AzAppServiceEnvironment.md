---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970080"
---
# <span data-ttu-id="c8941-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8941-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="c8941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8941-102">SYNOPSIS</span></span>
<span data-ttu-id="c8941-103">App Service Environment를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="c8941-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8941-104">SYNTAX</span></span>

### <span data-ttu-id="c8941-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8941-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8941-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8941-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8941-107">설명</span><span class="sxs-lookup"><span data-stu-id="c8941-107">DESCRIPTION</span></span>
<span data-ttu-id="c8941-108">**Remove-AzAppServiceEnvironment** cmdlet은 App Service 환경을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="c8941-109">모든 App Service 계획은 ASE를 삭제하기 전에 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="c8941-110">예제</span><span class="sxs-lookup"><span data-stu-id="c8941-110">EXAMPLES</span></span>

### <span data-ttu-id="c8941-111">예제 1: App Service Environment 삭제</span><span class="sxs-lookup"><span data-stu-id="c8941-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="c8941-112">App Service Environment 삭제</span><span class="sxs-lookup"><span data-stu-id="c8941-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="c8941-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8941-113">PARAMETERS</span></span>

### <span data-ttu-id="c8941-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8941-114">-AsJob</span></span>
<span data-ttu-id="c8941-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c8941-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8941-116">-DefaultProfile</span></span>
<span data-ttu-id="c8941-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8941-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c8941-118">-Force</span></span>
<span data-ttu-id="c8941-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c8941-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8941-120">-InputObject</span></span>
<span data-ttu-id="c8941-121">앱 서비스 환경 개체</span><span class="sxs-lookup"><span data-stu-id="c8941-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8941-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c8941-122">-Name</span></span>
<span data-ttu-id="c8941-123">앱 서비스 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8941-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8941-124">-PassThru</span></span>
<span data-ttu-id="c8941-125">상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-125">Return status.</span></span>

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

### <span data-ttu-id="c8941-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8941-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8941-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8941-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c8941-128">-Confirm</span></span>
<span data-ttu-id="c8941-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8941-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8941-130">-WhatIf</span></span>
<span data-ttu-id="c8941-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8941-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8941-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8941-133">CommonParameters</span></span>
<span data-ttu-id="c8941-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8941-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8941-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8941-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8941-136">입력</span><span class="sxs-lookup"><span data-stu-id="c8941-136">INPUTS</span></span>

### <span data-ttu-id="c8941-137">없음</span><span class="sxs-lookup"><span data-stu-id="c8941-137">None</span></span>

## <span data-ttu-id="c8941-138">출력</span><span class="sxs-lookup"><span data-stu-id="c8941-138">OUTPUTS</span></span>

### <span data-ttu-id="c8941-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="c8941-139">System.Object</span></span>
## <span data-ttu-id="c8941-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8941-140">NOTES</span></span>

## <span data-ttu-id="c8941-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8941-141">RELATED LINKS</span></span>

[<span data-ttu-id="c8941-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8941-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="c8941-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8941-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="c8941-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="c8941-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)