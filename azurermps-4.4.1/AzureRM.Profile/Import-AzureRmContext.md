---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530718"
---
# <span data-ttu-id="ff593-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ff593-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="ff593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff593-102">SYNOPSIS</span></span>
<span data-ttu-id="ff593-103">파일에서 Azure 인증 정보를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff593-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff593-104">SYNTAX</span></span>

### <span data-ttu-id="ff593-105">ProfileFromDisk (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff593-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff593-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="ff593-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff593-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff593-107">DESCRIPTION</span></span>
<span data-ttu-id="ff593-108">Import-AzureRmContext cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="ff593-109">현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="ff593-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ff593-110">EXAMPLES</span></span>

### <span data-ttu-id="ff593-111">예제 1: AzureRmProfile에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff593-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ff593-112">이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile에서 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="ff593-113">예제 2: JSON 파일에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff593-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ff593-114">이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 컨텍스트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="ff593-115">이 JSON 파일은 Save-AzureRmContext에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="ff593-116">변수</span><span class="sxs-lookup"><span data-stu-id="ff593-116">PARAMETERS</span></span>

### <span data-ttu-id="ff593-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="ff593-117">-AzureContext</span></span>
<span data-ttu-id="ff593-118">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="ff593-119">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff593-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff593-120">-DefaultProfile</span></span>
<span data-ttu-id="ff593-121">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff593-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff593-122">-Path</span><span class="sxs-lookup"><span data-stu-id="ff593-122">-Path</span></span>
<span data-ttu-id="ff593-123">Save-AzureRMContext를 사용 하 여 저장 된 컨텍스트 정보의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff593-124">-범위</span><span class="sxs-lookup"><span data-stu-id="ff593-124">-Scope</span></span>
<span data-ttu-id="ff593-125">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff593-126">-확인</span><span class="sxs-lookup"><span data-stu-id="ff593-126">-Confirm</span></span>
<span data-ttu-id="ff593-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff593-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff593-128">-WhatIf</span></span>
<span data-ttu-id="ff593-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff593-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff593-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff593-131">CommonParameters</span></span>
<span data-ttu-id="ff593-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff593-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff593-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff593-134">입력</span><span class="sxs-lookup"><span data-stu-id="ff593-134">INPUTS</span></span>

### <span data-ttu-id="ff593-135">AzureRMProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="ff593-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="ff593-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정 및 구독의 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="ff593-137">출력</span><span class="sxs-lookup"><span data-stu-id="ff593-137">OUTPUTS</span></span>

### <span data-ttu-id="ff593-138">Microsoft. Azure. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ff593-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="ff593-139">Azure와 통신 하는 데 사용할 수 있는 자격 증명, 계정 및 구독의 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff593-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="ff593-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ff593-140">NOTES</span></span>

## <span data-ttu-id="ff593-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff593-141">RELATED LINKS</span></span>

