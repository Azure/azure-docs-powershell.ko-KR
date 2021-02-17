---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190497"
---
# <span data-ttu-id="75847-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="75847-101">Get-AzDefault</span></span>

## <span data-ttu-id="75847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75847-102">SYNOPSIS</span></span>
<span data-ttu-id="75847-103">현재 컨텍스트에서 사용자가 설정한 기본값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75847-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="75847-104">구문</span><span class="sxs-lookup"><span data-stu-id="75847-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75847-105">설명</span><span class="sxs-lookup"><span data-stu-id="75847-105">DESCRIPTION</span></span>
<span data-ttu-id="75847-106">Get-AzDefault cmdlet은 사용자가 현재 컨텍스트에서 기본값으로 설정한 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75847-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="75847-107">예제</span><span class="sxs-lookup"><span data-stu-id="75847-107">EXAMPLES</span></span>

### <span data-ttu-id="75847-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="75847-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="75847-109">이 명령은 기본값이 설정되어 있는 경우 현재 기본값을 반환하거나 기본값이 설정되지 않았다면 아무 것도 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75847-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="75847-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="75847-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="75847-111">이 명령은 기본 집합이 있는 경우 현재 기본 리소스 그룹을 반환하거나 기본값이 설정되지 않았다면 아무 것도 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75847-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="75847-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75847-112">PARAMETERS</span></span>

### <span data-ttu-id="75847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75847-113">-DefaultProfile</span></span>
<span data-ttu-id="75847-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75847-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75847-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75847-115">-ResourceGroup</span></span>
<span data-ttu-id="75847-116">기본 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="75847-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75847-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75847-117">CommonParameters</span></span>
<span data-ttu-id="75847-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75847-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75847-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="75847-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75847-120">입력</span><span class="sxs-lookup"><span data-stu-id="75847-120">INPUTS</span></span>

### <span data-ttu-id="75847-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75847-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75847-122">출력</span><span class="sxs-lookup"><span data-stu-id="75847-122">OUTPUTS</span></span>

### <span data-ttu-id="75847-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75847-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="75847-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75847-124">NOTES</span></span>

## <span data-ttu-id="75847-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75847-125">RELATED LINKS</span></span>
