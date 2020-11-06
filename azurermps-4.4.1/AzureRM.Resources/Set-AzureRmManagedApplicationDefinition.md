---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527304"
---
# <span data-ttu-id="4ee5c-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="4ee5c-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="4ee5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee5c-103">관리 되는 응용 프로그램 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="4ee5c-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ee5c-104">SYNTAX</span></span>

### <span data-ttu-id="4ee5c-105">관리 되는 응용 프로그램 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="4ee5c-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="4ee5c-106">기본값</span><span class="sxs-lookup"><span data-stu-id="4ee5c-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ee5c-107">관리 되는 응용 프로그램 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="4ee5c-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee5c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4ee5c-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee5c-109">**AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="4ee5c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4ee5c-110">EXAMPLES</span></span>

### <span data-ttu-id="4ee5c-111">예제 1: 관리 되는 응용 프로그램 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="4ee5c-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="4ee5c-112">이 명령은 관리 되는 응용 프로그램 정의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="4ee5c-113">변수</span><span class="sxs-lookup"><span data-stu-id="4ee5c-113">PARAMETERS</span></span>

### <span data-ttu-id="4ee5c-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ee5c-114">-ApiVersion</span></span>
<span data-ttu-id="4ee5c-115">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4ee5c-116">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4ee5c-117">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="4ee5c-117">-Authorization</span></span>
<span data-ttu-id="4ee5c-118">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-118">The managed application definition authorization.</span></span>
<span data-ttu-id="4ee5c-119">다음과 같은 형식으로 쉼표로 구분 된 인증 쌍 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="4ee5c-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee5c-120">-DefaultProfile</span></span>
<span data-ttu-id="4ee5c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee5c-122">-설명</span><span class="sxs-lookup"><span data-stu-id="4ee5c-122">-Description</span></span>
<span data-ttu-id="4ee5c-123">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="4ee5c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4ee5c-124">-DisplayName</span></span>
<span data-ttu-id="4ee5c-125">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="4ee5c-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4ee5c-126">-Name</span></span>
<span data-ttu-id="4ee5c-127">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee5c-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="4ee5c-128">-PackageFileUri</span></span>
<span data-ttu-id="4ee5c-129">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="4ee5c-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ee5c-130">-Pre</span></span>
<span data-ttu-id="4ee5c-131">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4ee5c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee5c-132">-ResourceGroupName</span></span>
<span data-ttu-id="4ee5c-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee5c-134">태그</span><span class="sxs-lookup"><span data-stu-id="4ee5c-134">-Tag</span></span>
<span data-ttu-id="4ee5c-135">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4ee5c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="4ee5c-136">-Confirm</span></span>
<span data-ttu-id="4ee5c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee5c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee5c-138">-WhatIf</span></span>
<span data-ttu-id="4ee5c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee5c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee5c-141">-Id</span><span class="sxs-lookup"><span data-stu-id="4ee5c-141">-Id</span></span>
<span data-ttu-id="4ee5c-142">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="4ee5c-143">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4ee5c-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee5c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee5c-144">CommonParameters</span></span>
<span data-ttu-id="4ee5c-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ee5c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee5c-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee5c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee5c-147">입력</span><span class="sxs-lookup"><span data-stu-id="4ee5c-147">INPUTS</span></span>

### <span data-ttu-id="4ee5c-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ee5c-148">System.String</span></span>
<span data-ttu-id="4ee5c-149">System. String [] System.webserver</span><span class="sxs-lookup"><span data-stu-id="4ee5c-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ee5c-150">출력</span><span class="sxs-lookup"><span data-stu-id="4ee5c-150">OUTPUTS</span></span>

### <span data-ttu-id="4ee5c-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="4ee5c-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4ee5c-152">상속자</span><span class="sxs-lookup"><span data-stu-id="4ee5c-152">NOTES</span></span>

## <span data-ttu-id="4ee5c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ee5c-153">RELATED LINKS</span></span>

