---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186404"
---
# <span data-ttu-id="60785-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="60785-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="60785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60785-102">SYNOPSIS</span></span>
<span data-ttu-id="60785-103">관리되는 애플리케이션 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60785-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="60785-104">구문</span><span class="sxs-lookup"><span data-stu-id="60785-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60785-105">설명</span><span class="sxs-lookup"><span data-stu-id="60785-105">DESCRIPTION</span></span>
<span data-ttu-id="60785-106">**New-AzManagedApplicationDefinition** cmdlet은 관리되는 애플리케이션 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60785-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="60785-107">예제</span><span class="sxs-lookup"><span data-stu-id="60785-107">EXAMPLES</span></span>

### <span data-ttu-id="60785-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="60785-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="60785-109">이 명령은 관리되는 애플리케이션 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60785-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="60785-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60785-110">PARAMETERS</span></span>

### <span data-ttu-id="60785-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60785-111">-ApiVersion</span></span>
<span data-ttu-id="60785-112">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60785-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="60785-113">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="60785-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="60785-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="60785-114">-Authorization</span></span>
<span data-ttu-id="60785-115">관리되는 애플리케이션 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-115">The managed application definition authorization.</span></span>
<span data-ttu-id="60785-116">콤마로 구분된 권한 부여 쌍은 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="60785-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60785-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="60785-117">-CreateUiDefinition</span></span>
<span data-ttu-id="60785-118">관리되는 애플리케이션 정의 만들기 UI 정의</span><span class="sxs-lookup"><span data-stu-id="60785-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="60785-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60785-119">-DefaultProfile</span></span>
<span data-ttu-id="60785-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60785-121">-Description</span><span class="sxs-lookup"><span data-stu-id="60785-121">-Description</span></span>
<span data-ttu-id="60785-122">관리되는 애플리케이션 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="60785-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60785-123">-DisplayName</span></span>
<span data-ttu-id="60785-124">관리되는 애플리케이션 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="60785-125">-Location</span><span class="sxs-lookup"><span data-stu-id="60785-125">-Location</span></span>
<span data-ttu-id="60785-126">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-126">The resource location.</span></span>

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

### <span data-ttu-id="60785-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="60785-127">-LockLevel</span></span>
<span data-ttu-id="60785-128">관리되는 애플리케이션 정의에 대한 잠금 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60785-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="60785-129">-MainTemplate</span></span>
<span data-ttu-id="60785-130">관리되는 애플리케이션 정의 기본 템플릿</span><span class="sxs-lookup"><span data-stu-id="60785-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="60785-131">-Name</span><span class="sxs-lookup"><span data-stu-id="60785-131">-Name</span></span>
<span data-ttu-id="60785-132">관리되는 애플리케이션 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="60785-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="60785-133">-PackageFileUri</span></span>
<span data-ttu-id="60785-134">관리되는 애플리케이션 정의 패키지 파일 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="60785-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="60785-135">-Pre</span></span>
<span data-ttu-id="60785-136">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="60785-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="60785-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60785-137">-ResourceGroupName</span></span>
<span data-ttu-id="60785-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-138">The resource group name.</span></span>

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

### <span data-ttu-id="60785-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="60785-139">-Tag</span></span>
<span data-ttu-id="60785-140">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="60785-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="60785-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60785-141">-Confirm</span></span>
<span data-ttu-id="60785-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="60785-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60785-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60785-143">-WhatIf</span></span>
<span data-ttu-id="60785-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="60785-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60785-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60785-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60785-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60785-146">CommonParameters</span></span>
<span data-ttu-id="60785-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="60785-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60785-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60785-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60785-149">입력</span><span class="sxs-lookup"><span data-stu-id="60785-149">INPUTS</span></span>

### <span data-ttu-id="60785-150">System.String</span><span class="sxs-lookup"><span data-stu-id="60785-150">System.String</span></span>

### <span data-ttu-id="60785-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="60785-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="60785-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="60785-152">System.String[]</span></span>

### <span data-ttu-id="60785-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="60785-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60785-154">출력</span><span class="sxs-lookup"><span data-stu-id="60785-154">OUTPUTS</span></span>

### <span data-ttu-id="60785-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="60785-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="60785-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="60785-156">NOTES</span></span>

## <span data-ttu-id="60785-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60785-157">RELATED LINKS</span></span>
