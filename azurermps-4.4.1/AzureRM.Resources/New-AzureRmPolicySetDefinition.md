---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703629"
---
# <span data-ttu-id="b0eba-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b0eba-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b0eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0eba-102">SYNOPSIS</span></span>
<span data-ttu-id="b0eba-103">정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0eba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0eba-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0eba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0eba-105">DESCRIPTION</span></span>
<span data-ttu-id="b0eba-106">**새 AzureRmPolicySetDefinition** cmdlet은 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="b0eba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0eba-107">EXAMPLES</span></span>

### <span data-ttu-id="b0eba-108">예제 1: 정책 집합 파일을 사용 하 여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="b0eba-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="b0eba-109">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 VMPolicyDefinition 이라는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="b0eba-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0eba-110">PARAMETERS</span></span>

### <span data-ttu-id="b0eba-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b0eba-111">-ApiVersion</span></span>
<span data-ttu-id="b0eba-112">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b0eba-113">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b0eba-114">-설명</span><span class="sxs-lookup"><span data-stu-id="b0eba-114">-Description</span></span>
<span data-ttu-id="b0eba-115">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-115">The description for policy set definition.</span></span>

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

### <span data-ttu-id="b0eba-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b0eba-116">-DisplayName</span></span>
<span data-ttu-id="b0eba-117">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-117">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="b0eba-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b0eba-118">-Name</span></span>
<span data-ttu-id="b0eba-119">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-119">The policy set definition name.</span></span>

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

### <span data-ttu-id="b0eba-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b0eba-120">-Parameter</span></span>
<span data-ttu-id="b0eba-121">정책 집합 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="b0eba-122">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="b0eba-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0eba-123">-PolicyDefinition</span></span>
<span data-ttu-id="b0eba-124">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-124">The policy set definition.</span></span> <span data-ttu-id="b0eba-125">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="b0eba-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b0eba-126">-Pre</span></span>
<span data-ttu-id="b0eba-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0eba-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b0eba-128">-Confirm</span></span>
<span data-ttu-id="b0eba-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0eba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0eba-130">-DefaultProfile</span></span>
<span data-ttu-id="b0eba-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0eba-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b0eba-132">-Metadata</span></span>
<span data-ttu-id="b0eba-133">정책 집합 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-133">The metadata for policy set definition.</span></span> <span data-ttu-id="b0eba-134">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터 인 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="b0eba-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0eba-135">-WhatIf</span></span>
<span data-ttu-id="b0eba-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0eba-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0eba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0eba-138">CommonParameters</span></span>
<span data-ttu-id="b0eba-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0eba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0eba-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0eba-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0eba-141">입력</span><span class="sxs-lookup"><span data-stu-id="b0eba-141">INPUTS</span></span>

### <span data-ttu-id="b0eba-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0eba-142">System.String</span></span>

## <span data-ttu-id="b0eba-143">출력</span><span class="sxs-lookup"><span data-stu-id="b0eba-143">OUTPUTS</span></span>

### <span data-ttu-id="b0eba-144">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="b0eba-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b0eba-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b0eba-145">NOTES</span></span>

## <span data-ttu-id="b0eba-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0eba-146">RELATED LINKS</span></span>

