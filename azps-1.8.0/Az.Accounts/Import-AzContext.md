---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 145c5f65b00da7f143b04d526b8bcd959d323d12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689249"
---
# <span data-ttu-id="be8ff-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="be8ff-101">Import-AzContext</span></span>

## <span data-ttu-id="be8ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="be8ff-103">파일에서 Azure 인증 정보를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="be8ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be8ff-104">SYNTAX</span></span>

### <span data-ttu-id="be8ff-105">ProfileFromDisk (기본값)</span><span class="sxs-lookup"><span data-stu-id="be8ff-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be8ff-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="be8ff-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be8ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="be8ff-107">DESCRIPTION</span></span>
<span data-ttu-id="be8ff-108">Import-AzContext cmdlet은 파일에서 인증 정보를 로드 하 여 Azure 환경 및 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="be8ff-109">현재 세션에서 실행 하는 cmdlet은이 정보를 사용 하 여 Azure Resource Manager에 대 한 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="be8ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="be8ff-110">EXAMPLES</span></span>

### <span data-ttu-id="be8ff-111">예제 1: AzureRmProfile에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="be8ff-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="be8ff-112">이 예제에서는 cmdlet으로 전달 되는 PSAzureProfile에서 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="be8ff-113">예제 2: JSON 파일에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="be8ff-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="be8ff-114">이 예제에서는 cmdlet으로 전달 되는 JSON 파일에서 컨텍스트를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="be8ff-115">이 JSON 파일은 Save-AzContext에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="be8ff-116">변수</span><span class="sxs-lookup"><span data-stu-id="be8ff-116">PARAMETERS</span></span>

### <span data-ttu-id="be8ff-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="be8ff-117">-AzureContext</span></span>
<span data-ttu-id="be8ff-118">{{Fill의 AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="be8ff-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="be8ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be8ff-119">-DefaultProfile</span></span>
<span data-ttu-id="be8ff-120">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be8ff-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be8ff-121">-Path</span><span class="sxs-lookup"><span data-stu-id="be8ff-121">-Path</span></span>
<span data-ttu-id="be8ff-122">Save-AzContext를 사용 하 여 저장 된 컨텍스트 정보의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="be8ff-123">-범위</span><span class="sxs-lookup"><span data-stu-id="be8ff-123">-Scope</span></span>
<span data-ttu-id="be8ff-124">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="be8ff-125">-확인</span><span class="sxs-lookup"><span data-stu-id="be8ff-125">-Confirm</span></span>
<span data-ttu-id="be8ff-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be8ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be8ff-127">-WhatIf</span></span>
<span data-ttu-id="be8ff-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be8ff-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be8ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be8ff-130">CommonParameters</span></span>
<span data-ttu-id="be8ff-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be8ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be8ff-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be8ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be8ff-133">입력</span><span class="sxs-lookup"><span data-stu-id="be8ff-133">INPUTS</span></span>

### <span data-ttu-id="be8ff-134">AzureRmProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="be8ff-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="be8ff-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be8ff-135">System.String</span></span>

## <span data-ttu-id="be8ff-136">출력</span><span class="sxs-lookup"><span data-stu-id="be8ff-136">OUTPUTS</span></span>

### <span data-ttu-id="be8ff-137">Microsoft. Azure. a PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="be8ff-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="be8ff-138">상속자</span><span class="sxs-lookup"><span data-stu-id="be8ff-138">NOTES</span></span>

## <span data-ttu-id="be8ff-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be8ff-139">RELATED LINKS</span></span>
