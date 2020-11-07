---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703365"
---
# <span data-ttu-id="adbed-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="adbed-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="adbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adbed-102">SYNOPSIS</span></span>
<span data-ttu-id="adbed-103">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adbed-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adbed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adbed-105">DESCRIPTION</span></span>
<span data-ttu-id="adbed-106">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="adbed-107">IotHub의 총, 사용 가능, 사용 불가능 장치 수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="adbed-108">예제의</span><span class="sxs-lookup"><span data-stu-id="adbed-108">EXAMPLES</span></span>

### <span data-ttu-id="adbed-109">예제 1 RegistryStatistics 가져오기</span><span class="sxs-lookup"><span data-stu-id="adbed-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="adbed-110">"Myiothub" IotHub에 대 한 RegistryStatictics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="adbed-111">변수</span><span class="sxs-lookup"><span data-stu-id="adbed-111">PARAMETERS</span></span>

### <span data-ttu-id="adbed-112">-이름</span><span class="sxs-lookup"><span data-stu-id="adbed-112">-Name</span></span>
<span data-ttu-id="adbed-113">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-113">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="adbed-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbed-114">-ResourceGroupName</span></span>
<span data-ttu-id="adbed-115">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="adbed-115">Resource Group Name</span></span>

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

### <span data-ttu-id="adbed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbed-116">-DefaultProfile</span></span>
<span data-ttu-id="adbed-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adbed-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbed-118">CommonParameters</span></span>
<span data-ttu-id="adbed-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adbed-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbed-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbed-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbed-121">입력</span><span class="sxs-lookup"><span data-stu-id="adbed-121">INPUTS</span></span>

### <span data-ttu-id="adbed-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adbed-122">System.String</span></span>

## <span data-ttu-id="adbed-123">출력</span><span class="sxs-lookup"><span data-stu-id="adbed-123">OUTPUTS</span></span>

### <span data-ttu-id="adbed-124">System.webserver. IList ' 1 [[IotHub. PSIotHubRegistryStatistics, IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]) ")")</span><span class="sxs-lookup"><span data-stu-id="adbed-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="adbed-125">상속자</span><span class="sxs-lookup"><span data-stu-id="adbed-125">NOTES</span></span>

## <span data-ttu-id="adbed-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adbed-126">RELATED LINKS</span></span>

