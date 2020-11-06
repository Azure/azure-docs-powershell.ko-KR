---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535872"
---
# <span data-ttu-id="87cbb-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="87cbb-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="87cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="87cbb-103">Azure IoT Hub를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87cbb-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87cbb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="87cbb-106">IotHub의 태그 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="87cbb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87cbb-107">EXAMPLES</span></span>

### <span data-ttu-id="87cbb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="87cbb-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="87cbb-109">@tagsAzure IoT Hub "myiotdps" 태그에 ""를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="87cbb-110">변수</span><span class="sxs-lookup"><span data-stu-id="87cbb-110">PARAMETERS</span></span>

### <span data-ttu-id="87cbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cbb-111">-DefaultProfile</span></span>
<span data-ttu-id="87cbb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87cbb-113">-이름</span><span class="sxs-lookup"><span data-stu-id="87cbb-113">-Name</span></span>
<span data-ttu-id="87cbb-114">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="87cbb-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="87cbb-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="87cbb-115">-Reset</span></span>
<span data-ttu-id="87cbb-116">IoTHub 태그 다시 설정</span><span class="sxs-lookup"><span data-stu-id="87cbb-116">Reset IoTHub Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cbb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87cbb-117">-ResourceGroupName</span></span>
<span data-ttu-id="87cbb-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87cbb-119">태그</span><span class="sxs-lookup"><span data-stu-id="87cbb-119">-Tag</span></span>
<span data-ttu-id="87cbb-120">IoTHub 태그 모음</span><span class="sxs-lookup"><span data-stu-id="87cbb-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cbb-121">-확인</span><span class="sxs-lookup"><span data-stu-id="87cbb-121">-Confirm</span></span>
<span data-ttu-id="87cbb-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cbb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87cbb-123">-WhatIf</span></span>
<span data-ttu-id="87cbb-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87cbb-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cbb-126">CommonParameters</span></span>
<span data-ttu-id="87cbb-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87cbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cbb-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87cbb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cbb-129">입력</span><span class="sxs-lookup"><span data-stu-id="87cbb-129">INPUTS</span></span>

### <span data-ttu-id="87cbb-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87cbb-130">System.String</span></span>

## <span data-ttu-id="87cbb-131">출력</span><span class="sxs-lookup"><span data-stu-id="87cbb-131">OUTPUTS</span></span>

### <span data-ttu-id="87cbb-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="87cbb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="87cbb-133">상속자</span><span class="sxs-lookup"><span data-stu-id="87cbb-133">NOTES</span></span>

## <span data-ttu-id="87cbb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87cbb-134">RELATED LINKS</span></span>
