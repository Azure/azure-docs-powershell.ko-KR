---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 286dcf7812f3ca796c8d2049112aa2cc64f96bd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876439"
---
# <span data-ttu-id="6728b-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6728b-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="6728b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6728b-102">SYNOPSIS</span></span>
<span data-ttu-id="6728b-103">관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="6728b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6728b-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6728b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6728b-105">DESCRIPTION</span></span>
<span data-ttu-id="6728b-106">**AzManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="6728b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6728b-107">EXAMPLES</span></span>

### <span data-ttu-id="6728b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6728b-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="6728b-109">이 명령은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="6728b-110">변수</span><span class="sxs-lookup"><span data-stu-id="6728b-110">PARAMETERS</span></span>

### <span data-ttu-id="6728b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6728b-111">-ApiVersion</span></span>
<span data-ttu-id="6728b-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6728b-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6728b-114">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="6728b-114">-Authorization</span></span>
<span data-ttu-id="6728b-115">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-115">The managed application definition authorization.</span></span>
<span data-ttu-id="6728b-116">\<Principalid \> : \< roleDefinitionId의 형식으로 쉼표로 구분 된 인증 쌍\></span><span class="sxs-lookup"><span data-stu-id="6728b-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="6728b-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="6728b-117">-CreateUiDefinition</span></span>
<span data-ttu-id="6728b-118">관리 되는 응용 프로그램 정의 ui 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="6728b-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="6728b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6728b-119">-DefaultProfile</span></span>
<span data-ttu-id="6728b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6728b-121">-설명</span><span class="sxs-lookup"><span data-stu-id="6728b-121">-Description</span></span>
<span data-ttu-id="6728b-122">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="6728b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6728b-123">-DisplayName</span></span>
<span data-ttu-id="6728b-124">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="6728b-125">-위치</span><span class="sxs-lookup"><span data-stu-id="6728b-125">-Location</span></span>
<span data-ttu-id="6728b-126">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-126">The resource location.</span></span>

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

### <span data-ttu-id="6728b-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="6728b-127">-LockLevel</span></span>
<span data-ttu-id="6728b-128">관리 되는 응용 프로그램 정의에 대 한 잠금 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="6728b-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="6728b-129">-MainTemplate</span></span>
<span data-ttu-id="6728b-130">관리 되는 응용 프로그램 정의 기본 서식 파일</span><span class="sxs-lookup"><span data-stu-id="6728b-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="6728b-131">-이름</span><span class="sxs-lookup"><span data-stu-id="6728b-131">-Name</span></span>
<span data-ttu-id="6728b-132">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="6728b-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="6728b-133">-PackageFileUri</span></span>
<span data-ttu-id="6728b-134">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="6728b-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6728b-135">-Pre</span></span>
<span data-ttu-id="6728b-136">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6728b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6728b-137">-ResourceGroupName</span></span>
<span data-ttu-id="6728b-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-138">The resource group name.</span></span>

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

### <span data-ttu-id="6728b-139">태그</span><span class="sxs-lookup"><span data-stu-id="6728b-139">-Tag</span></span>
<span data-ttu-id="6728b-140">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6728b-141">-확인</span><span class="sxs-lookup"><span data-stu-id="6728b-141">-Confirm</span></span>
<span data-ttu-id="6728b-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6728b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6728b-143">-WhatIf</span></span>
<span data-ttu-id="6728b-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6728b-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6728b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6728b-146">CommonParameters</span></span>
<span data-ttu-id="6728b-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6728b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6728b-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6728b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6728b-149">입력</span><span class="sxs-lookup"><span data-stu-id="6728b-149">INPUTS</span></span>

### <span data-ttu-id="6728b-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6728b-150">System.String</span></span>

### <span data-ttu-id="6728b-151">Microsoft. Azure.. a i m.</span><span class="sxs-lookup"><span data-stu-id="6728b-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="6728b-152">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6728b-152">System.String[]</span></span>

### <span data-ttu-id="6728b-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6728b-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6728b-154">출력</span><span class="sxs-lookup"><span data-stu-id="6728b-154">OUTPUTS</span></span>

### <span data-ttu-id="6728b-155">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="6728b-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6728b-156">상속자</span><span class="sxs-lookup"><span data-stu-id="6728b-156">NOTES</span></span>

## <span data-ttu-id="6728b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6728b-157">RELATED LINKS</span></span>
