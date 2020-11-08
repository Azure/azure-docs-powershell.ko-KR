---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042001"
---
# <span data-ttu-id="c9c00-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c00-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="c9c00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c00-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c00-103">지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c9c00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9c00-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9c00-105">DESCRIPTION</span></span>
<span data-ttu-id="c9c00-106">Remove-AzEnvironment cmdlet은 지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c9c00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9c00-107">EXAMPLES</span></span>

### <span data-ttu-id="c9c00-108">예제 1: 테스트 환경 만들기 및 제거</span><span class="sxs-lookup"><span data-stu-id="c9c00-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="c9c00-109">이 예제에서는 AzEnvironment를 사용 하 여 환경을 만드는 방법과 Remove-AzEnvironment를 사용 하 여 환경을 삭제 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="c9c00-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9c00-110">PARAMETERS</span></span>

### <span data-ttu-id="c9c00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c00-111">-DefaultProfile</span></span>
<span data-ttu-id="c9c00-112">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9c00-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c9c00-113">-Name</span></span>
<span data-ttu-id="c9c00-114">제거할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="c9c00-115">-범위</span><span class="sxs-lookup"><span data-stu-id="c9c00-115">-Scope</span></span>
<span data-ttu-id="c9c00-116">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c9c00-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c9c00-117">-Confirm</span></span>
<span data-ttu-id="c9c00-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c00-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c00-119">-WhatIf</span></span>
<span data-ttu-id="c9c00-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9c00-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c00-122">CommonParameters</span></span>
<span data-ttu-id="c9c00-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c00-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c00-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c00-125">입력</span><span class="sxs-lookup"><span data-stu-id="c9c00-125">INPUTS</span></span>

### <span data-ttu-id="c9c00-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9c00-126">System.String</span></span>

## <span data-ttu-id="c9c00-127">출력</span><span class="sxs-lookup"><span data-stu-id="c9c00-127">OUTPUTS</span></span>

### <span data-ttu-id="c9c00-128">Microsoft. Azure. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c00-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c9c00-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c9c00-129">NOTES</span></span>

## <span data-ttu-id="c9c00-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9c00-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9c00-131">추가-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c00-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c9c00-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c00-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c9c00-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c9c00-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

