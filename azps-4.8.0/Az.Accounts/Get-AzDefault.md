---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211919"
---
# <span data-ttu-id="7b5be-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="7b5be-101">Get-AzDefault</span></span>

## <span data-ttu-id="7b5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5be-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5be-103">사용자가 현재 컨텍스트에서 설정한 기본값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="7b5be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b5be-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b5be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b5be-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5be-106">Get-AzDefault cmdlet은 사용자가 현재 컨텍스트에서 기본값으로 설정한 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="7b5be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b5be-107">EXAMPLES</span></span>

### <span data-ttu-id="7b5be-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b5be-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="7b5be-109">이 명령은 기본값이 설정 된 경우 현재 기본값을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="7b5be-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="7b5be-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="7b5be-111">기본 집합이 있는 경우이 명령은 현재 기본 리소스 그룹을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="7b5be-112">변수</span><span class="sxs-lookup"><span data-stu-id="7b5be-112">PARAMETERS</span></span>

### <span data-ttu-id="7b5be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5be-113">-DefaultProfile</span></span>
<span data-ttu-id="7b5be-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b5be-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b5be-115">-ResourceGroup</span></span>
<span data-ttu-id="7b5be-116">기본 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="7b5be-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="7b5be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5be-117">CommonParameters</span></span>
<span data-ttu-id="7b5be-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b5be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5be-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b5be-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5be-120">입력</span><span class="sxs-lookup"><span data-stu-id="7b5be-120">INPUTS</span></span>

### <span data-ttu-id="7b5be-121">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b5be-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b5be-122">출력</span><span class="sxs-lookup"><span data-stu-id="7b5be-122">OUTPUTS</span></span>

### <span data-ttu-id="7b5be-123">Microsoft. Azure. PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7b5be-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="7b5be-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7b5be-124">NOTES</span></span>

## <span data-ttu-id="7b5be-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b5be-125">RELATED LINKS</span></span>
