---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 5acba21e8daf1adaa83820d67c5955b27230c4ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954912"
---
# <span data-ttu-id="fd071-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fd071-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="fd071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd071-102">SYNOPSIS</span></span>
<span data-ttu-id="fd071-103">주어진 Azure 인스턴스에 연결하기 위한 엔드포인트 및 메타데이터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="fd071-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd071-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd071-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd071-105">DESCRIPTION</span></span>
<span data-ttu-id="fd071-106">Remove-AzEnvironment cmdlet은 주어진 Azure 인스턴스에 연결하기 위한 엔드포인트 및 메타데이터 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="fd071-107">예제</span><span class="sxs-lookup"><span data-stu-id="fd071-107">EXAMPLES</span></span>

### <span data-ttu-id="fd071-108">예제 1: 테스트 환경 만들기 및 제거</span><span class="sxs-lookup"><span data-stu-id="fd071-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="fd071-109">이 예제에서는 Add-AzEnvironment을 사용하여 환경을 만든 다음 Remove-AzEnvironment을 사용하여 환경을 삭제하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="fd071-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd071-110">PARAMETERS</span></span>

### <span data-ttu-id="fd071-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd071-111">-DefaultProfile</span></span>
<span data-ttu-id="fd071-112">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd071-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fd071-113">-Name</span></span>
<span data-ttu-id="fd071-114">제거할 환경의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd071-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="fd071-115">-Scope</span></span>
<span data-ttu-id="fd071-116">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="fd071-117">-확인</span><span class="sxs-lookup"><span data-stu-id="fd071-117">-Confirm</span></span>
<span data-ttu-id="fd071-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd071-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd071-119">-WhatIf</span></span>
<span data-ttu-id="fd071-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd071-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd071-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd071-122">CommonParameters</span></span>
<span data-ttu-id="fd071-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd071-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd071-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd071-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd071-125">입력</span><span class="sxs-lookup"><span data-stu-id="fd071-125">INPUTS</span></span>

### <span data-ttu-id="fd071-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fd071-126">System.String</span></span>

## <span data-ttu-id="fd071-127">출력</span><span class="sxs-lookup"><span data-stu-id="fd071-127">OUTPUTS</span></span>

### <span data-ttu-id="fd071-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="fd071-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="fd071-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd071-129">NOTES</span></span>

## <span data-ttu-id="fd071-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd071-130">RELATED LINKS</span></span>

[<span data-ttu-id="fd071-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fd071-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="fd071-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fd071-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="fd071-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="fd071-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

