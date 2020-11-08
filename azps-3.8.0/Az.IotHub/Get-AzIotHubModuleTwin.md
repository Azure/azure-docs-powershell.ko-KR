---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043835"
---
# <span data-ttu-id="d56ce-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="d56ce-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="d56ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d56ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d56ce-103">IoT 장치 모듈 트윈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="d56ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d56ce-104">SYNTAX</span></span>

### <span data-ttu-id="d56ce-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d56ce-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d56ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d56ce-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d56ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d56ce-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d56ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d56ce-108">DESCRIPTION</span></span>
<span data-ttu-id="d56ce-109">IoT 장치 모듈 트윈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="d56ce-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d56ce-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="d56ce-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d56ce-111">EXAMPLES</span></span>

### <span data-ttu-id="d56ce-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d56ce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="d56ce-113">장치 모듈 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="d56ce-114">변수</span><span class="sxs-lookup"><span data-stu-id="d56ce-114">PARAMETERS</span></span>

### <span data-ttu-id="d56ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56ce-115">-DefaultProfile</span></span>
<span data-ttu-id="d56ce-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56ce-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d56ce-117">-DeviceId</span></span>
<span data-ttu-id="d56ce-118">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d56ce-119">-InputObject</span></span>
<span data-ttu-id="d56ce-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d56ce-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d56ce-121">-IotHubName</span></span>
<span data-ttu-id="d56ce-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d56ce-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="d56ce-123">-ModuleId</span></span>
<span data-ttu-id="d56ce-124">대상 모듈 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="d56ce-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d56ce-127">-ResourceId</span></span>
<span data-ttu-id="d56ce-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="d56ce-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56ce-129">CommonParameters</span></span>
<span data-ttu-id="d56ce-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d56ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56ce-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56ce-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56ce-132">입력</span><span class="sxs-lookup"><span data-stu-id="d56ce-132">INPUTS</span></span>

### <span data-ttu-id="d56ce-133">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="d56ce-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d56ce-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d56ce-134">System.String</span></span>

## <span data-ttu-id="d56ce-135">출력</span><span class="sxs-lookup"><span data-stu-id="d56ce-135">OUTPUTS</span></span>

### <span data-ttu-id="d56ce-136">IotHub. PSModuleTwin/. \*</span><span class="sxs-lookup"><span data-stu-id="d56ce-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="d56ce-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d56ce-137">NOTES</span></span>

## <span data-ttu-id="d56ce-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d56ce-138">RELATED LINKS</span></span>
