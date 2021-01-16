---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333141"
---
# <span data-ttu-id="a4dfb-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="a4dfb-101">Import-AzContext</span></span>

## <span data-ttu-id="a4dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dfb-103">파일에서 Azure 인증 정보를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a4dfb-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4dfb-104">SYNTAX</span></span>

### <span data-ttu-id="a4dfb-105">ProfileFromDisk(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4dfb-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4dfb-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="a4dfb-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dfb-107">설명</span><span class="sxs-lookup"><span data-stu-id="a4dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="a4dfb-108">이 Import-AzContext cmdlet은 파일에서 인증 정보를 로드하여 Azure 환경 및 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a4dfb-109">현재 세션에서 실행한 Cmdlet은 이 정보를 사용하여 Azure Resource Manager에 대한 요청을 인증합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a4dfb-110">예제</span><span class="sxs-lookup"><span data-stu-id="a4dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="a4dfb-111">예제 1: AzureRmProfile에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="a4dfb-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a4dfb-112">이 예제에서는 cmdlet을 통해 전달된 PSAzureProfile에서 컨텍스트를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a4dfb-113">예제 2: JSON 파일에서 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="a4dfb-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a4dfb-114">이 예제에서는 cmdlet에 전달된 JSON 파일에서 컨텍스트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="a4dfb-115">이 JSON 파일은 Save-AzContext에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="a4dfb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4dfb-116">PARAMETERS</span></span>

### <span data-ttu-id="a4dfb-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="a4dfb-117">-AzureContext</span></span>
<span data-ttu-id="a4dfb-118">{{AzureContext 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="a4dfb-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="a4dfb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dfb-119">-DefaultProfile</span></span>
<span data-ttu-id="a4dfb-120">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a4dfb-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4dfb-121">-Path</span><span class="sxs-lookup"><span data-stu-id="a4dfb-121">-Path</span></span>
<span data-ttu-id="a4dfb-122">Save-AzContext를 사용하여 저장된 컨텍스트 정보에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="a4dfb-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="a4dfb-123">-Scope</span></span>
<span data-ttu-id="a4dfb-124">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a4dfb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4dfb-125">-Confirm</span></span>
<span data-ttu-id="a4dfb-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dfb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dfb-127">-WhatIf</span></span>
<span data-ttu-id="a4dfb-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a4dfb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4dfb-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dfb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dfb-130">CommonParameters</span></span>
<span data-ttu-id="a4dfb-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dfb-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4dfb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dfb-133">입력</span><span class="sxs-lookup"><span data-stu-id="a4dfb-133">INPUTS</span></span>

### <span data-ttu-id="a4dfb-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a4dfb-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="a4dfb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a4dfb-135">System.String</span></span>

## <span data-ttu-id="a4dfb-136">출력</span><span class="sxs-lookup"><span data-stu-id="a4dfb-136">OUTPUTS</span></span>

### <span data-ttu-id="a4dfb-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a4dfb-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="a4dfb-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4dfb-138">NOTES</span></span>

## <span data-ttu-id="a4dfb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4dfb-139">RELATED LINKS</span></span>
