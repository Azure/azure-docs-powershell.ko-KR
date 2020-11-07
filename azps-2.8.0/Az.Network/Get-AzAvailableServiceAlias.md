---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 7ea7bec01bacba43732f8e1eb544b109dfae11b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870234"
---
# <span data-ttu-id="870bc-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="870bc-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="870bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870bc-102">SYNOPSIS</span></span>
<span data-ttu-id="870bc-103">지역에서 사용 가능한 서비스 별칭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="870bc-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="870bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="870bc-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="870bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="870bc-105">DESCRIPTION</span></span>
<span data-ttu-id="870bc-106">**AzAvailableServiceAlias** cmdlet을 사용 하 여 제공 된 위치에서 서브넷에 대해 사용 가능한 모든 서비스 별칭을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870bc-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="870bc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="870bc-107">EXAMPLES</span></span>

### <span data-ttu-id="870bc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="870bc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="870bc-109">변수</span><span class="sxs-lookup"><span data-stu-id="870bc-109">PARAMETERS</span></span>

### <span data-ttu-id="870bc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870bc-110">-DefaultProfile</span></span>
<span data-ttu-id="870bc-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="870bc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="870bc-112">-위치</span><span class="sxs-lookup"><span data-stu-id="870bc-112">-Location</span></span>
<span data-ttu-id="870bc-113">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="870bc-113">The location.</span></span>

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

### <span data-ttu-id="870bc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870bc-114">CommonParameters</span></span>
<span data-ttu-id="870bc-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="870bc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870bc-116">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="870bc-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870bc-117">입력</span><span class="sxs-lookup"><span data-stu-id="870bc-117">INPUTS</span></span>

### <span data-ttu-id="870bc-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="870bc-118">System.String</span></span>

## <span data-ttu-id="870bc-119">출력</span><span class="sxs-lookup"><span data-stu-id="870bc-119">OUTPUTS</span></span>

### <span data-ttu-id="870bc-120">PsAvailableServiceAlias에 대 한.</span><span class="sxs-lookup"><span data-stu-id="870bc-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="870bc-121">상속자</span><span class="sxs-lookup"><span data-stu-id="870bc-121">NOTES</span></span>

## <span data-ttu-id="870bc-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="870bc-122">RELATED LINKS</span></span>
