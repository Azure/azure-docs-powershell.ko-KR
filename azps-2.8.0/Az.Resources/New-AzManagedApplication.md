---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 8286bdd365f43881f09787dfb051e873d2fdeb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873362"
---
# <span data-ttu-id="5ba0c-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="5ba0c-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="5ba0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba0c-103">Azure 관리 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="5ba0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ba0c-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ba0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ba0c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba0c-106">**AzManagedApplication** Cmdlet은 Azure 관리 되는 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="5ba0c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5ba0c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba0c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ba0c-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="5ba0c-109">이 명령은 관리 되는 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-109">This command creates a managed application</span></span>

## <span data-ttu-id="5ba0c-110">변수</span><span class="sxs-lookup"><span data-stu-id="5ba0c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba0c-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ba0c-111">-ApiVersion</span></span>
<span data-ttu-id="5ba0c-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5ba0c-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba0c-114">-DefaultProfile</span></span>
<span data-ttu-id="5ba0c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba0c-116">-종류</span><span class="sxs-lookup"><span data-stu-id="5ba0c-116">-Kind</span></span>
<span data-ttu-id="5ba0c-117">관리 되는 응용 프로그램 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-117">The managed application kind.</span></span>
<span data-ttu-id="5ba0c-118">마켓플레이스 또는 servicecatalog 중 하나</span><span class="sxs-lookup"><span data-stu-id="5ba0c-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-119">-위치</span><span class="sxs-lookup"><span data-stu-id="5ba0c-119">-Location</span></span>
<span data-ttu-id="5ba0c-120">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-120">The resource location.</span></span>

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

### <span data-ttu-id="5ba0c-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5ba0c-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="5ba0c-122">관리 되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="5ba0c-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="5ba0c-124">관리 되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="5ba0c-125">-Name</span></span>
<span data-ttu-id="5ba0c-126">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5ba0c-127">-Parameter</span></span>
<span data-ttu-id="5ba0c-128">관리 되는 응용 프로그램에 대 한 매개 변수의 JSON 형식 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="5ba0c-129">이는 매개 변수를 포함 하는 uri 또는 파일 이름 또는 매개 변수를 문자열로 경로에 대 한 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="5ba0c-130">-계획</span><span class="sxs-lookup"><span data-stu-id="5ba0c-130">-Plan</span></span>
<span data-ttu-id="5ba0c-131">관리 되는 응용 프로그램 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="5ba0c-132">-Pre</span></span>
<span data-ttu-id="5ba0c-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ba0c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ba0c-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-136">태그</span><span class="sxs-lookup"><span data-stu-id="5ba0c-136">-Tag</span></span>
<span data-ttu-id="5ba0c-137">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba0c-138">-확인</span><span class="sxs-lookup"><span data-stu-id="5ba0c-138">-Confirm</span></span>
<span data-ttu-id="5ba0c-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba0c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba0c-140">-WhatIf</span></span>
<span data-ttu-id="5ba0c-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba0c-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba0c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba0c-143">CommonParameters</span></span>
<span data-ttu-id="5ba0c-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba0c-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba0c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba0c-146">입력</span><span class="sxs-lookup"><span data-stu-id="5ba0c-146">INPUTS</span></span>

### <span data-ttu-id="5ba0c-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ba0c-147">System.String</span></span>

### <span data-ttu-id="5ba0c-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5ba0c-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5ba0c-149">출력</span><span class="sxs-lookup"><span data-stu-id="5ba0c-149">OUTPUTS</span></span>

### <span data-ttu-id="5ba0c-150">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="5ba0c-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5ba0c-151">상속자</span><span class="sxs-lookup"><span data-stu-id="5ba0c-151">NOTES</span></span>

## <span data-ttu-id="5ba0c-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ba0c-152">RELATED LINKS</span></span>
