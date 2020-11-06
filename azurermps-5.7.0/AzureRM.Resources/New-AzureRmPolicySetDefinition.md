---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531662"
---
# <span data-ttu-id="99980-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="99980-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="99980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99980-102">SYNOPSIS</span></span>
<span data-ttu-id="99980-103">정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99980-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99980-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99980-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99980-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99980-105">DESCRIPTION</span></span>
<span data-ttu-id="99980-106">**새 AzureRmPolicySetDefinition** cmdlet은 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99980-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="99980-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99980-107">EXAMPLES</span></span>

### <span data-ttu-id="99980-108">예제 1: 정책 집합 파일을 사용 하 여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="99980-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="99980-109">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 VMPolicyDefinition 이라는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99980-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="99980-110">변수</span><span class="sxs-lookup"><span data-stu-id="99980-110">PARAMETERS</span></span>

### <span data-ttu-id="99980-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99980-111">-ApiVersion</span></span>
<span data-ttu-id="99980-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99980-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="99980-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99980-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99980-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99980-114">-DefaultProfile</span></span>
<span data-ttu-id="99980-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99980-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99980-116">-설명</span><span class="sxs-lookup"><span data-stu-id="99980-116">-Description</span></span>
<span data-ttu-id="99980-117">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-117">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99980-118">-DisplayName</span></span>
<span data-ttu-id="99980-119">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-119">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="99980-120">-Metadata</span></span>
<span data-ttu-id="99980-121">정책 집합 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-121">The metadata for policy set definition.</span></span> <span data-ttu-id="99980-122">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터를 string으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99980-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-123">-이름</span><span class="sxs-lookup"><span data-stu-id="99980-123">-Name</span></span>
<span data-ttu-id="99980-124">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-124">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="99980-125">-Parameter</span></span>
<span data-ttu-id="99980-126">정책 집합 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="99980-127">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99980-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="99980-128">-PolicyDefinition</span></span>
<span data-ttu-id="99980-129">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="99980-129">The policy set definition.</span></span> <span data-ttu-id="99980-130">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99980-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99980-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="99980-131">-Pre</span></span>
<span data-ttu-id="99980-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99980-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99980-133">-확인</span><span class="sxs-lookup"><span data-stu-id="99980-133">-Confirm</span></span>
<span data-ttu-id="99980-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99980-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99980-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99980-135">-WhatIf</span></span>
<span data-ttu-id="99980-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99980-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99980-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99980-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99980-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99980-138">CommonParameters</span></span>
<span data-ttu-id="99980-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99980-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99980-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99980-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99980-141">입력</span><span class="sxs-lookup"><span data-stu-id="99980-141">INPUTS</span></span>

### <span data-ttu-id="99980-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99980-142">System.String</span></span>

## <span data-ttu-id="99980-143">출력</span><span class="sxs-lookup"><span data-stu-id="99980-143">OUTPUTS</span></span>

### <span data-ttu-id="99980-144">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="99980-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="99980-145">상속자</span><span class="sxs-lookup"><span data-stu-id="99980-145">NOTES</span></span>

## <span data-ttu-id="99980-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99980-146">RELATED LINKS</span></span>
