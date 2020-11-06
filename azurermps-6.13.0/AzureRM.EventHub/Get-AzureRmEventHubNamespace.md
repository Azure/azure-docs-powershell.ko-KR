---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: 35f9342fa66b46cfd029d6440d8d82134a6822a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526191"
---
# <span data-ttu-id="b8d97-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b8d97-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="b8d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d97-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d97-103">이벤트 허브 네임 스페이스의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 허브 네임 스페이스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8d97-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8d97-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d97-106">Get-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 세부 정보 또는 현재 Azure 구독에서 모든 이벤트 허브 네임 스페이스의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="b8d97-107">네임 스페이스 이름을 제공 하는 경우 단일 이벤트 허브 네임 스페이스에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="b8d97-108">네임 스페이스 이름을 제공 하지 않으면 네임 스페이스 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="b8d97-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8d97-109">EXAMPLES</span></span>

### <span data-ttu-id="b8d97-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8d97-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b8d97-111">\` \` 리소스 그룹 MyResourceGroupName에서 네임 스페이스 MyNamespaceName의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="b8d97-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b8d97-112">변수</span><span class="sxs-lookup"><span data-stu-id="b8d97-112">PARAMETERS</span></span>

### <span data-ttu-id="b8d97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d97-113">-DefaultProfile</span></span>
<span data-ttu-id="b8d97-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d97-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b8d97-115">-Name</span></span>
<span data-ttu-id="b8d97-116">EventHub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b8d97-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d97-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8d97-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b8d97-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d97-119">CommonParameters</span></span>
<span data-ttu-id="b8d97-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d97-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d97-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d97-122">입력</span><span class="sxs-lookup"><span data-stu-id="b8d97-122">INPUTS</span></span>

### <span data-ttu-id="b8d97-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8d97-123">System.String</span></span>

## <span data-ttu-id="b8d97-124">출력</span><span class="sxs-lookup"><span data-stu-id="b8d97-124">OUTPUTS</span></span>

### <span data-ttu-id="b8d97-125">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="b8d97-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b8d97-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b8d97-126">NOTES</span></span>

## <span data-ttu-id="b8d97-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d97-127">RELATED LINKS</span></span>
