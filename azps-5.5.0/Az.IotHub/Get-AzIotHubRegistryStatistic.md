---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185641"
---
# <span data-ttu-id="d4e91-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="d4e91-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="d4e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e91-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e91-103">IotHub에 대한 RegistryStatistics를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="d4e91-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4e91-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e91-105">설명</span><span class="sxs-lookup"><span data-stu-id="d4e91-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e91-106">IotHub에 대한 RegistryStatistics를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="d4e91-107">IotHub에서 총, 사용 및 비활성화된 디바이스 수에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="d4e91-108">예제</span><span class="sxs-lookup"><span data-stu-id="d4e91-108">EXAMPLES</span></span>

### <span data-ttu-id="d4e91-109">예제 1 RegistryStatistics를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d4e91-110">"myiothub"라는 IotHub에 대한 RegistryStatistics를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d4e91-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4e91-111">PARAMETERS</span></span>

### <span data-ttu-id="d4e91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e91-112">-DefaultProfile</span></span>
<span data-ttu-id="d4e91-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d4e91-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e91-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e91-114">-Name</span></span>
<span data-ttu-id="d4e91-115">IoT Hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d4e91-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e91-116">-ResourceGroupName</span></span>
<span data-ttu-id="d4e91-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d4e91-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d4e91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e91-118">CommonParameters</span></span>
<span data-ttu-id="d4e91-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e91-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d4e91-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e91-121">입력</span><span class="sxs-lookup"><span data-stu-id="d4e91-121">INPUTS</span></span>

### <span data-ttu-id="d4e91-122">System.String</span><span class="sxs-lookup"><span data-stu-id="d4e91-122">System.String</span></span>

## <span data-ttu-id="d4e91-123">출력</span><span class="sxs-lookup"><span data-stu-id="d4e91-123">OUTPUTS</span></span>

### <span data-ttu-id="d4e91-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="d4e91-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="d4e91-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4e91-125">NOTES</span></span>

## <span data-ttu-id="d4e91-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4e91-126">RELATED LINKS</span></span>
