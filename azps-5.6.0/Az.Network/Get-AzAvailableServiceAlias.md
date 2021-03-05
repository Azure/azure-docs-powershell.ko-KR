---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 4eb210380feaaf101bad45b4bd0b4df26533f9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993897"
---
# <span data-ttu-id="f577e-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="f577e-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="f577e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f577e-102">SYNOPSIS</span></span>
<span data-ttu-id="f577e-103">지역에서 사용 가능한 서비스 별칭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f577e-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="f577e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f577e-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f577e-105">설명</span><span class="sxs-lookup"><span data-stu-id="f577e-105">DESCRIPTION</span></span>
<span data-ttu-id="f577e-106">**Get-AzAvailableServiceAlias** cmdlet을 사용하면 제공된 위치에서 서브넷에 사용할 수 있는 모든 서비스 별칭을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f577e-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="f577e-107">예제</span><span class="sxs-lookup"><span data-stu-id="f577e-107">EXAMPLES</span></span>

### <span data-ttu-id="f577e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f577e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="f577e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f577e-109">PARAMETERS</span></span>

### <span data-ttu-id="f577e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f577e-110">-DefaultProfile</span></span>
<span data-ttu-id="f577e-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f577e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f577e-112">-Location</span><span class="sxs-lookup"><span data-stu-id="f577e-112">-Location</span></span>
<span data-ttu-id="f577e-113">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f577e-113">The location.</span></span>

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

### <span data-ttu-id="f577e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f577e-114">CommonParameters</span></span>
<span data-ttu-id="f577e-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f577e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f577e-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f577e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f577e-117">입력</span><span class="sxs-lookup"><span data-stu-id="f577e-117">INPUTS</span></span>

### <span data-ttu-id="f577e-118">System.String</span><span class="sxs-lookup"><span data-stu-id="f577e-118">System.String</span></span>

## <span data-ttu-id="f577e-119">출력</span><span class="sxs-lookup"><span data-stu-id="f577e-119">OUTPUTS</span></span>

### <span data-ttu-id="f577e-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="f577e-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="f577e-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f577e-121">NOTES</span></span>

## <span data-ttu-id="f577e-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f577e-122">RELATED LINKS</span></span>
