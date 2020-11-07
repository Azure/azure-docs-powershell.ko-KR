---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 762987f39c1529b1b2c6dbce3325666704fd57fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711022"
---
# <span data-ttu-id="1df1f-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="1df1f-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="1df1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1df1f-102">SYNOPSIS</span></span>
<span data-ttu-id="1df1f-103">관리 되는 응용 프로그램 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="1df1f-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1df1f-104">SYNTAX</span></span>

### <span data-ttu-id="1df1f-105">SetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="1df1f-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1df1f-106">SetById</span><span class="sxs-lookup"><span data-stu-id="1df1f-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1df1f-107">DESCRIPTION</span></span>
<span data-ttu-id="1df1f-108">**AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="1df1f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1df1f-109">EXAMPLES</span></span>

### <span data-ttu-id="1df1f-110">예제 1: 관리 되는 응용 프로그램 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="1df1f-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="1df1f-111">이 명령은 관리 되는 응용 프로그램 정의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="1df1f-112">변수</span><span class="sxs-lookup"><span data-stu-id="1df1f-112">PARAMETERS</span></span>

### <span data-ttu-id="1df1f-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1df1f-113">-ApiVersion</span></span>
<span data-ttu-id="1df1f-114">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1df1f-115">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1df1f-116">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="1df1f-116">-Authorization</span></span>
<span data-ttu-id="1df1f-117">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-117">The managed application definition authorization.</span></span>
<span data-ttu-id="1df1f-118">다음과 같은 형식으로 쉼표로 구분 된 인증 쌍 \<principalId\>\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="1df1f-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="1df1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df1f-119">-DefaultProfile</span></span>
<span data-ttu-id="1df1f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df1f-121">-설명</span><span class="sxs-lookup"><span data-stu-id="1df1f-121">-Description</span></span>
<span data-ttu-id="1df1f-122">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="1df1f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1df1f-123">-DisplayName</span></span>
<span data-ttu-id="1df1f-124">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="1df1f-125">-Id</span><span class="sxs-lookup"><span data-stu-id="1df1f-125">-Id</span></span>
<span data-ttu-id="1df1f-126">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="1df1f-127">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df1f-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="1df1f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1df1f-128">-Name</span></span>
<span data-ttu-id="1df1f-129">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="1df1f-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="1df1f-130">-PackageFileUri</span></span>
<span data-ttu-id="1df1f-131">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="1df1f-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="1df1f-132">-Pre</span></span>
<span data-ttu-id="1df1f-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1df1f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df1f-134">-ResourceGroupName</span></span>
<span data-ttu-id="1df1f-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-135">The resource group name.</span></span>

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

### <span data-ttu-id="1df1f-136">태그</span><span class="sxs-lookup"><span data-stu-id="1df1f-136">-Tag</span></span>
<span data-ttu-id="1df1f-137">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1df1f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1df1f-138">-Confirm</span></span>
<span data-ttu-id="1df1f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1df1f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df1f-140">-WhatIf</span></span>
<span data-ttu-id="1df1f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1df1f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1df1f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df1f-143">CommonParameters</span></span>
<span data-ttu-id="1df1f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df1f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df1f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df1f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df1f-146">입력</span><span class="sxs-lookup"><span data-stu-id="1df1f-146">INPUTS</span></span>

### <span data-ttu-id="1df1f-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1df1f-147">System.String</span></span>

### <span data-ttu-id="1df1f-148">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="1df1f-148">System.String[]</span></span>

### <span data-ttu-id="1df1f-149">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1df1f-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1df1f-150">출력</span><span class="sxs-lookup"><span data-stu-id="1df1f-150">OUTPUTS</span></span>

### <span data-ttu-id="1df1f-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="1df1f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1df1f-152">상속자</span><span class="sxs-lookup"><span data-stu-id="1df1f-152">NOTES</span></span>

## <span data-ttu-id="1df1f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1df1f-153">RELATED LINKS</span></span>
