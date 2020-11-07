---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 3e929d2df0b2132b89f6ccff6b83020453b61ad2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875293"
---
# <span data-ttu-id="0df46-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="0df46-101">Get-AzDefault</span></span>

## <span data-ttu-id="0df46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df46-102">SYNOPSIS</span></span>
<span data-ttu-id="0df46-103">사용자가 현재 컨텍스트에서 설정한 기본값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="0df46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0df46-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0df46-105">DESCRIPTION</span></span>
<span data-ttu-id="0df46-106">Get-AzDefault cmdlet은 사용자가 현재 컨텍스트에서 기본값으로 설정한 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="0df46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0df46-107">EXAMPLES</span></span>

### <span data-ttu-id="0df46-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0df46-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0df46-109">이 명령은 기본값이 설정 된 경우 현재 기본값을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="0df46-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="0df46-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0df46-111">기본 집합이 있는 경우이 명령은 현재 기본 리소스 그룹을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="0df46-112">변수</span><span class="sxs-lookup"><span data-stu-id="0df46-112">PARAMETERS</span></span>

### <span data-ttu-id="0df46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df46-113">-DefaultProfile</span></span>
<span data-ttu-id="0df46-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0df46-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0df46-115">-ResourceGroup</span></span>
<span data-ttu-id="0df46-116">기본 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="0df46-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="0df46-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df46-117">CommonParameters</span></span>
<span data-ttu-id="0df46-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df46-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df46-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df46-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df46-120">입력</span><span class="sxs-lookup"><span data-stu-id="0df46-120">INPUTS</span></span>

### <span data-ttu-id="0df46-121">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0df46-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0df46-122">출력</span><span class="sxs-lookup"><span data-stu-id="0df46-122">OUTPUTS</span></span>

### <span data-ttu-id="0df46-123">Microsoft. Azure. PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0df46-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="0df46-124">상속자</span><span class="sxs-lookup"><span data-stu-id="0df46-124">NOTES</span></span>

## <span data-ttu-id="0df46-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0df46-125">RELATED LINKS</span></span>
