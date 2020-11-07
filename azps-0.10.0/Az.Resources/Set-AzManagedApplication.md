---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 7370facc2b0891a4fe378180ba65cabddeba316b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876365"
---
# <span data-ttu-id="850e1-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="850e1-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="850e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850e1-102">SYNOPSIS</span></span>
<span data-ttu-id="850e1-103">업데이트 관리 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="850e1-103">Updates managed application</span></span>

## <span data-ttu-id="850e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="850e1-104">SYNTAX</span></span>

### <span data-ttu-id="850e1-105">SetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="850e1-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="850e1-106">SetById</span><span class="sxs-lookup"><span data-stu-id="850e1-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="850e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="850e1-107">DESCRIPTION</span></span>
<span data-ttu-id="850e1-108">**AzManagedApplication** cmdlet은 관리 되는 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="850e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="850e1-109">EXAMPLES</span></span>

### <span data-ttu-id="850e1-110">예제 1: 관리 되는 응용 프로그램 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="850e1-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="850e1-111">이 명령은 관리 되는 응용 프로그램 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-111">This command updates the managed application description</span></span>

## <span data-ttu-id="850e1-112">변수</span><span class="sxs-lookup"><span data-stu-id="850e1-112">PARAMETERS</span></span>

### <span data-ttu-id="850e1-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="850e1-113">-ApiVersion</span></span>
<span data-ttu-id="850e1-114">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="850e1-115">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="850e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850e1-116">-DefaultProfile</span></span>
<span data-ttu-id="850e1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850e1-118">-Id</span><span class="sxs-lookup"><span data-stu-id="850e1-118">-Id</span></span>
<span data-ttu-id="850e1-119">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="850e1-120">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850e1-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850e1-121">-종류</span><span class="sxs-lookup"><span data-stu-id="850e1-121">-Kind</span></span>
<span data-ttu-id="850e1-122">관리 되는 응용 프로그램 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-122">The managed application kind.</span></span>
<span data-ttu-id="850e1-123">마켓플레이스 또는 servicecatalog 중 하나</span><span class="sxs-lookup"><span data-stu-id="850e1-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="850e1-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="850e1-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="850e1-125">관리 되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="850e1-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850e1-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="850e1-127">관리 되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="850e1-128">-이름</span><span class="sxs-lookup"><span data-stu-id="850e1-128">-Name</span></span>
<span data-ttu-id="850e1-129">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850e1-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="850e1-130">-Parameter</span></span>
<span data-ttu-id="850e1-131">관리 되는 응용 프로그램에 대 한 매개 변수의 JSON 형식 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="850e1-132">이는 매개 변수를 포함 하는 uri 또는 파일 이름 또는 매개 변수를 문자열로 경로에 대 한 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="850e1-133">-계획</span><span class="sxs-lookup"><span data-stu-id="850e1-133">-Plan</span></span>
<span data-ttu-id="850e1-134">관리 되는 응용 프로그램 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="850e1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="850e1-135">-Pre</span></span>
<span data-ttu-id="850e1-136">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="850e1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850e1-137">-ResourceGroupName</span></span>
<span data-ttu-id="850e1-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="850e1-139">태그</span><span class="sxs-lookup"><span data-stu-id="850e1-139">-Tag</span></span>
<span data-ttu-id="850e1-140">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="850e1-141">-확인</span><span class="sxs-lookup"><span data-stu-id="850e1-141">-Confirm</span></span>
<span data-ttu-id="850e1-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="850e1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="850e1-143">-WhatIf</span></span>
<span data-ttu-id="850e1-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="850e1-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="850e1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850e1-146">CommonParameters</span></span>
<span data-ttu-id="850e1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="850e1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850e1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="850e1-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850e1-149">입력</span><span class="sxs-lookup"><span data-stu-id="850e1-149">INPUTS</span></span>

### <span data-ttu-id="850e1-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="850e1-150">System.String</span></span>

### <span data-ttu-id="850e1-151">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="850e1-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="850e1-152">출력</span><span class="sxs-lookup"><span data-stu-id="850e1-152">OUTPUTS</span></span>

### <span data-ttu-id="850e1-153">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="850e1-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="850e1-154">상속자</span><span class="sxs-lookup"><span data-stu-id="850e1-154">NOTES</span></span>

## <span data-ttu-id="850e1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="850e1-155">RELATED LINKS</span></span>
