---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047658"
---
# <span data-ttu-id="fca39-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="fca39-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="fca39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fca39-102">SYNOPSIS</span></span>
<span data-ttu-id="fca39-103">관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="fca39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fca39-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca39-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fca39-105">DESCRIPTION</span></span>
<span data-ttu-id="fca39-106">**AzManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="fca39-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fca39-107">EXAMPLES</span></span>

### <span data-ttu-id="fca39-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fca39-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="fca39-109">이 명령은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="fca39-110">변수</span><span class="sxs-lookup"><span data-stu-id="fca39-110">PARAMETERS</span></span>

### <span data-ttu-id="fca39-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fca39-111">-ApiVersion</span></span>
<span data-ttu-id="fca39-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fca39-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fca39-114">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="fca39-114">-Authorization</span></span>
<span data-ttu-id="fca39-115">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-115">The managed application definition authorization.</span></span>
<span data-ttu-id="fca39-116">다음과 같은 형식으로 쉼표로 구분 된 인증 쌍 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="fca39-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="fca39-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="fca39-117">-CreateUiDefinition</span></span>
<span data-ttu-id="fca39-118">관리 되는 응용 프로그램 정의 ui 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="fca39-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="fca39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca39-119">-DefaultProfile</span></span>
<span data-ttu-id="fca39-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fca39-121">-설명</span><span class="sxs-lookup"><span data-stu-id="fca39-121">-Description</span></span>
<span data-ttu-id="fca39-122">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="fca39-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fca39-123">-DisplayName</span></span>
<span data-ttu-id="fca39-124">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="fca39-125">-위치</span><span class="sxs-lookup"><span data-stu-id="fca39-125">-Location</span></span>
<span data-ttu-id="fca39-126">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-126">The resource location.</span></span>

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

### <span data-ttu-id="fca39-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="fca39-127">-LockLevel</span></span>
<span data-ttu-id="fca39-128">관리 되는 응용 프로그램 정의에 대 한 잠금 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="fca39-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="fca39-129">-MainTemplate</span></span>
<span data-ttu-id="fca39-130">관리 되는 응용 프로그램 정의 기본 서식 파일</span><span class="sxs-lookup"><span data-stu-id="fca39-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="fca39-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fca39-131">-Name</span></span>
<span data-ttu-id="fca39-132">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="fca39-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="fca39-133">-PackageFileUri</span></span>
<span data-ttu-id="fca39-134">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="fca39-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="fca39-135">-Pre</span></span>
<span data-ttu-id="fca39-136">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fca39-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca39-137">-ResourceGroupName</span></span>
<span data-ttu-id="fca39-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-138">The resource group name.</span></span>

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

### <span data-ttu-id="fca39-139">태그</span><span class="sxs-lookup"><span data-stu-id="fca39-139">-Tag</span></span>
<span data-ttu-id="fca39-140">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fca39-141">-확인</span><span class="sxs-lookup"><span data-stu-id="fca39-141">-Confirm</span></span>
<span data-ttu-id="fca39-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca39-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca39-143">-WhatIf</span></span>
<span data-ttu-id="fca39-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca39-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca39-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca39-146">CommonParameters</span></span>
<span data-ttu-id="fca39-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca39-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca39-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fca39-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca39-149">입력</span><span class="sxs-lookup"><span data-stu-id="fca39-149">INPUTS</span></span>

### <span data-ttu-id="fca39-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fca39-150">System.String</span></span>

### <span data-ttu-id="fca39-151">Microsoft. Azure.. a i m.</span><span class="sxs-lookup"><span data-stu-id="fca39-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="fca39-152">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="fca39-152">System.String[]</span></span>

### <span data-ttu-id="fca39-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="fca39-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fca39-154">출력</span><span class="sxs-lookup"><span data-stu-id="fca39-154">OUTPUTS</span></span>

### <span data-ttu-id="fca39-155">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="fca39-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fca39-156">상속자</span><span class="sxs-lookup"><span data-stu-id="fca39-156">NOTES</span></span>

## <span data-ttu-id="fca39-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fca39-157">RELATED LINKS</span></span>
