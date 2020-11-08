---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043825"
---
# <span data-ttu-id="8ec4b-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="8ec4b-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="8ec4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec4b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec4b-103">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="8ec4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ec4b-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ec4b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec4b-106">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="8ec4b-107">IotHub의 총, 사용 가능, 사용 불가능 장치 수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="8ec4b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8ec4b-108">EXAMPLES</span></span>

### <span data-ttu-id="8ec4b-109">예제 1 RegistryStatistics 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ec4b-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8ec4b-110">"Myiothub" IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8ec4b-111">변수</span><span class="sxs-lookup"><span data-stu-id="8ec4b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ec4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec4b-112">-DefaultProfile</span></span>
<span data-ttu-id="8ec4b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8ec4b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ec4b-114">-이름</span><span class="sxs-lookup"><span data-stu-id="8ec4b-114">-Name</span></span>
<span data-ttu-id="8ec4b-115">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-115">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec4b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec4b-116">-ResourceGroupName</span></span>
<span data-ttu-id="8ec4b-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8ec4b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="8ec4b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec4b-118">CommonParameters</span></span>
<span data-ttu-id="8ec4b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec4b-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec4b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec4b-121">입력</span><span class="sxs-lookup"><span data-stu-id="8ec4b-121">INPUTS</span></span>

### <span data-ttu-id="8ec4b-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ec4b-122">System.String</span></span>

## <span data-ttu-id="8ec4b-123">출력</span><span class="sxs-lookup"><span data-stu-id="8ec4b-123">OUTPUTS</span></span>

### <span data-ttu-id="8ec4b-124">IotHub. PSIotHubRegistryStatistics/. \*</span><span class="sxs-lookup"><span data-stu-id="8ec4b-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="8ec4b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8ec4b-125">NOTES</span></span>

## <span data-ttu-id="8ec4b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ec4b-126">RELATED LINKS</span></span>