---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338114"
---
# <span data-ttu-id="c3301-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="c3301-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="c3301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3301-102">SYNOPSIS</span></span>
<span data-ttu-id="c3301-103">지역에서 사용 가능한 서비스 별칭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c3301-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="c3301-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3301-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3301-105">설명</span><span class="sxs-lookup"><span data-stu-id="c3301-105">DESCRIPTION</span></span>
<span data-ttu-id="c3301-106">**Get-AzAvailableServiceAlias** cmdlet을 사용하면 제공된 위치에서 서브넷에 사용 가능한 모든 서비스 별칭을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3301-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="c3301-107">예제</span><span class="sxs-lookup"><span data-stu-id="c3301-107">EXAMPLES</span></span>

### <span data-ttu-id="c3301-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3301-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="c3301-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3301-109">PARAMETERS</span></span>

### <span data-ttu-id="c3301-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3301-110">-DefaultProfile</span></span>
<span data-ttu-id="c3301-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3301-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3301-112">-Location</span><span class="sxs-lookup"><span data-stu-id="c3301-112">-Location</span></span>
<span data-ttu-id="c3301-113">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c3301-113">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3301-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3301-114">CommonParameters</span></span>
<span data-ttu-id="c3301-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3301-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3301-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3301-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3301-117">입력</span><span class="sxs-lookup"><span data-stu-id="c3301-117">INPUTS</span></span>

### <span data-ttu-id="c3301-118">System.String</span><span class="sxs-lookup"><span data-stu-id="c3301-118">System.String</span></span>

## <span data-ttu-id="c3301-119">출력</span><span class="sxs-lookup"><span data-stu-id="c3301-119">OUTPUTS</span></span>

### <span data-ttu-id="c3301-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="c3301-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="c3301-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3301-121">NOTES</span></span>

## <span data-ttu-id="c3301-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3301-122">RELATED LINKS</span></span>
