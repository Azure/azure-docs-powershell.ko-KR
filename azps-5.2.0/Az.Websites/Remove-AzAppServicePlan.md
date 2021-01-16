---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367060"
---
# <span data-ttu-id="0dc32-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="0dc32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc32-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc32-103">Azure App Service 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0dc32-104">구문</span><span class="sxs-lookup"><span data-stu-id="0dc32-104">SYNTAX</span></span>

### <span data-ttu-id="0dc32-105">S1</span><span class="sxs-lookup"><span data-stu-id="0dc32-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc32-106">S2</span><span class="sxs-lookup"><span data-stu-id="0dc32-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc32-107">설명</span><span class="sxs-lookup"><span data-stu-id="0dc32-107">DESCRIPTION</span></span>
<span data-ttu-id="0dc32-108">**Remove-AzAppServicePlan** cmdlet은 Azure App Service 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="0dc32-109">예제</span><span class="sxs-lookup"><span data-stu-id="0dc32-109">EXAMPLES</span></span>

### <span data-ttu-id="0dc32-110">예제 1: App Service 계획 제거</span><span class="sxs-lookup"><span data-stu-id="0dc32-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0dc32-111">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoASP라는 Azure App Service 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0dc32-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dc32-112">PARAMETERS</span></span>

### <span data-ttu-id="0dc32-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-113">-AppServicePlan</span></span>
<span data-ttu-id="0dc32-114">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="0dc32-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc32-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dc32-115">-AsJob</span></span>
<span data-ttu-id="0dc32-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0dc32-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dc32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc32-117">-DefaultProfile</span></span>
<span data-ttu-id="0dc32-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dc32-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0dc32-119">-Force</span></span>
<span data-ttu-id="0dc32-120">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="0dc32-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0dc32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0dc32-121">-Name</span></span>
<span data-ttu-id="0dc32-122">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="0dc32-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc32-123">-ResourceGroupName</span></span>
<span data-ttu-id="0dc32-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0dc32-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc32-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dc32-125">-Confirm</span></span>
<span data-ttu-id="0dc32-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc32-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc32-127">-WhatIf</span></span>
<span data-ttu-id="0dc32-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0dc32-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc32-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc32-130">CommonParameters</span></span>
<span data-ttu-id="0dc32-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc32-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0dc32-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc32-133">입력</span><span class="sxs-lookup"><span data-stu-id="0dc32-133">INPUTS</span></span>

### <span data-ttu-id="0dc32-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0dc32-135">출력</span><span class="sxs-lookup"><span data-stu-id="0dc32-135">OUTPUTS</span></span>

### <span data-ttu-id="0dc32-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0dc32-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0dc32-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0dc32-137">NOTES</span></span>

## <span data-ttu-id="0dc32-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dc32-138">RELATED LINKS</span></span>

[<span data-ttu-id="0dc32-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="0dc32-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="0dc32-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0dc32-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


