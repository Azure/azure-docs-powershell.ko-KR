---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: bb4ab11406a644d34bdb5b45ea3b3fba47376826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868109"
---
# <span data-ttu-id="60b5f-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="60b5f-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="60b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="60b5f-103">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="60b5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60b5f-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b5f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="60b5f-106">IotHub에 대 한 RegistryStatistics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="60b5f-107">IotHub의 총, 사용 가능, 사용 불가능 장치 수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="60b5f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="60b5f-108">EXAMPLES</span></span>

### <span data-ttu-id="60b5f-109">예제 1 RegistryStatistics 가져오기</span><span class="sxs-lookup"><span data-stu-id="60b5f-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="60b5f-110">"Myiothub" IotHub에 대 한 RegistryStatictics를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="60b5f-111">변수</span><span class="sxs-lookup"><span data-stu-id="60b5f-111">PARAMETERS</span></span>

### <span data-ttu-id="60b5f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b5f-112">-DefaultProfile</span></span>
<span data-ttu-id="60b5f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60b5f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60b5f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="60b5f-114">-Name</span></span>
<span data-ttu-id="60b5f-115">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="60b5f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b5f-116">-ResourceGroupName</span></span>
<span data-ttu-id="60b5f-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="60b5f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="60b5f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b5f-118">CommonParameters</span></span>
<span data-ttu-id="60b5f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60b5f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b5f-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b5f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b5f-121">입력</span><span class="sxs-lookup"><span data-stu-id="60b5f-121">INPUTS</span></span>

### <span data-ttu-id="60b5f-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60b5f-122">System.String</span></span>

## <span data-ttu-id="60b5f-123">출력</span><span class="sxs-lookup"><span data-stu-id="60b5f-123">OUTPUTS</span></span>

### <span data-ttu-id="60b5f-124">IotHub. PSIotHubRegistryStatistics/. \*</span><span class="sxs-lookup"><span data-stu-id="60b5f-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="60b5f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="60b5f-125">NOTES</span></span>

## <span data-ttu-id="60b5f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60b5f-126">RELATED LINKS</span></span>
