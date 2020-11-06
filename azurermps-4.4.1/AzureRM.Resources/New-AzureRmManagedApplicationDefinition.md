---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536980"
---
# <span data-ttu-id="41d65-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="41d65-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="41d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d65-102">SYNOPSIS</span></span>
<span data-ttu-id="41d65-103">관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41d65-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41d65-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41d65-105">DESCRIPTION</span></span>
<span data-ttu-id="41d65-106">**AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="41d65-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41d65-107">EXAMPLES</span></span>

### <span data-ttu-id="41d65-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="41d65-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="41d65-109">이 명령은 관리 되는 응용 프로그램 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="41d65-110">변수</span><span class="sxs-lookup"><span data-stu-id="41d65-110">PARAMETERS</span></span>

### <span data-ttu-id="41d65-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="41d65-111">-ApiVersion</span></span>
<span data-ttu-id="41d65-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="41d65-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="41d65-114">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="41d65-114">-Authorization</span></span>
<span data-ttu-id="41d65-115">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-115">The managed application definition authorization.</span></span>
<span data-ttu-id="41d65-116">다음과 같은 형식으로 쉼표로 구분 된 인증 쌍 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="41d65-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="41d65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d65-117">-DefaultProfile</span></span>
<span data-ttu-id="41d65-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d65-119">-설명</span><span class="sxs-lookup"><span data-stu-id="41d65-119">-Description</span></span>
<span data-ttu-id="41d65-120">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-120">The managed application definition description.</span></span>

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

### <span data-ttu-id="41d65-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="41d65-121">-DisplayName</span></span>
<span data-ttu-id="41d65-122">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-122">The managed application definition display name.</span></span>

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

### <span data-ttu-id="41d65-123">-위치</span><span class="sxs-lookup"><span data-stu-id="41d65-123">-Location</span></span>
<span data-ttu-id="41d65-124">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-124">The resource location.</span></span>

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

### <span data-ttu-id="41d65-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="41d65-125">-LockLevel</span></span>
<span data-ttu-id="41d65-126">관리 되는 응용 프로그램 정의에 대 한 잠금 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-126">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="41d65-127">-이름</span><span class="sxs-lookup"><span data-stu-id="41d65-127">-Name</span></span>
<span data-ttu-id="41d65-128">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-128">The managed application definition name.</span></span>

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

### <span data-ttu-id="41d65-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="41d65-129">-PackageFileUri</span></span>
<span data-ttu-id="41d65-130">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-130">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="41d65-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="41d65-131">-Pre</span></span>
<span data-ttu-id="41d65-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="41d65-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d65-133">-ResourceGroupName</span></span>
<span data-ttu-id="41d65-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-134">The resource group name.</span></span>

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

### <span data-ttu-id="41d65-135">태그</span><span class="sxs-lookup"><span data-stu-id="41d65-135">-Tag</span></span>
<span data-ttu-id="41d65-136">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="41d65-137">-확인</span><span class="sxs-lookup"><span data-stu-id="41d65-137">-Confirm</span></span>
<span data-ttu-id="41d65-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d65-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d65-139">-WhatIf</span></span>
<span data-ttu-id="41d65-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d65-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d65-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="41d65-142">-CreateUiDefinition</span></span>
<span data-ttu-id="41d65-143">관리 되는 응용 프로그램 정의 ui 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-143">The managed application definition create ui definition.</span></span>

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

### <span data-ttu-id="41d65-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="41d65-144">-MainTemplate</span></span>
<span data-ttu-id="41d65-145">관리 되는 응용 프로그램 정의 기본 서식 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-145">The managed application definition main template.</span></span>

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

### <span data-ttu-id="41d65-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d65-146">CommonParameters</span></span>
<span data-ttu-id="41d65-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41d65-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d65-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d65-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d65-149">입력</span><span class="sxs-lookup"><span data-stu-id="41d65-149">INPUTS</span></span>

### <span data-ttu-id="41d65-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41d65-150">System.String</span></span>
<span data-ttu-id="41d65-151">Microsoft. Azure.. a i m. a i m. a i m. a i m.</span><span class="sxs-lookup"><span data-stu-id="41d65-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="41d65-152">출력</span><span class="sxs-lookup"><span data-stu-id="41d65-152">OUTPUTS</span></span>

### <span data-ttu-id="41d65-153">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="41d65-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="41d65-154">상속자</span><span class="sxs-lookup"><span data-stu-id="41d65-154">NOTES</span></span>

## <span data-ttu-id="41d65-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41d65-155">RELATED LINKS</span></span>

