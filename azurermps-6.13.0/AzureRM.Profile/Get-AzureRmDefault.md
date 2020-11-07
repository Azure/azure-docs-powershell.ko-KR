---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 7430402d62d88ea192b94166f48c0657e47cbf15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702238"
---
# <span data-ttu-id="0b96b-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="0b96b-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="0b96b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b96b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b96b-103">사용자가 현재 컨텍스트에서 설정한 기본값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b96b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b96b-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b96b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b96b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b96b-106">Get-AzureRmDefault cmdlet은 사용자가 현재 컨텍스트에서 기본값으로 설정한 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="0b96b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b96b-107">EXAMPLES</span></span>

### <span data-ttu-id="0b96b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b96b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0b96b-109">이 명령은 기본값이 설정 된 경우 현재 기본값을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="0b96b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="0b96b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0b96b-111">기본 집합이 있는 경우이 명령은 현재 기본 리소스 그룹을 반환 하 고, 기본값이 설정 되어 있지 않으면 nothing을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="0b96b-112">변수</span><span class="sxs-lookup"><span data-stu-id="0b96b-112">PARAMETERS</span></span>

### <span data-ttu-id="0b96b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b96b-113">-DefaultProfile</span></span>
<span data-ttu-id="0b96b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b96b-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0b96b-115">-ResourceGroup</span></span>
<span data-ttu-id="0b96b-116">기본 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="0b96b-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="0b96b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b96b-117">CommonParameters</span></span>
<span data-ttu-id="0b96b-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b96b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b96b-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b96b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b96b-120">입력</span><span class="sxs-lookup"><span data-stu-id="0b96b-120">INPUTS</span></span>

### <span data-ttu-id="0b96b-121">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b96b-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b96b-122">출력</span><span class="sxs-lookup"><span data-stu-id="0b96b-122">OUTPUTS</span></span>

### <span data-ttu-id="0b96b-123">Microsoft. Azure. PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0b96b-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="0b96b-124">상속자</span><span class="sxs-lookup"><span data-stu-id="0b96b-124">NOTES</span></span>

## <span data-ttu-id="0b96b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b96b-125">RELATED LINKS</span></span>
