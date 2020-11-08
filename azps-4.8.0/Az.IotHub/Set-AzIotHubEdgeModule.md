---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056319"
---
# <span data-ttu-id="1e3c5-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="1e3c5-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="1e3c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3c5-103">단일 edge 장치에서 edge 모듈을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="1e3c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e3c5-104">SYNTAX</span></span>

### <span data-ttu-id="1e3c5-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e3c5-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e3c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e3c5-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e3c5-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3c5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1e3c5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e3c5-109">제공 된 모듈 구성 콘텐츠를 지정한 edge 장치에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="1e3c5-110">참고: 실행할 때 명령은 장치에 적용 되는 모듈의 컬렉션을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="1e3c5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1e3c5-111">EXAMPLES</span></span>

### <span data-ttu-id="1e3c5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e3c5-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="1e3c5-113">대상 디바이스에서 모듈을 설정 하 여 개발 중에 edge 모듈을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="1e3c5-114">변수</span><span class="sxs-lookup"><span data-stu-id="1e3c5-114">PARAMETERS</span></span>

### <span data-ttu-id="1e3c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3c5-115">-DefaultProfile</span></span>
<span data-ttu-id="1e3c5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e3c5-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1e3c5-117">-DeviceId</span></span>
<span data-ttu-id="1e3c5-118">대상에 지 디바이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="1e3c5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e3c5-119">-InputObject</span></span>
<span data-ttu-id="1e3c5-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1e3c5-120">IotHub object</span></span>

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

### <span data-ttu-id="1e3c5-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1e3c5-121">-IotHubName</span></span>
<span data-ttu-id="1e3c5-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1e3c5-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1e3c5-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="1e3c5-123">-ModulesContent</span></span>
<span data-ttu-id="1e3c5-124">IoT Edge 장치에 대 한 모듈의 구성 콘텐츠입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="1e3c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="1e3c5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1e3c5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3c5-127">-ResourceId</span></span>
<span data-ttu-id="1e3c5-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="1e3c5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1e3c5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1e3c5-129">-Confirm</span></span>
<span data-ttu-id="1e3c5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3c5-131">-WhatIf</span></span>
<span data-ttu-id="1e3c5-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3c5-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3c5-134">CommonParameters</span></span>
<span data-ttu-id="1e3c5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3c5-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3c5-137">입력</span><span class="sxs-lookup"><span data-stu-id="1e3c5-137">INPUTS</span></span>

### <span data-ttu-id="1e3c5-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="1e3c5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1e3c5-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e3c5-139">System.String</span></span>

## <span data-ttu-id="1e3c5-140">출력</span><span class="sxs-lookup"><span data-stu-id="1e3c5-140">OUTPUTS</span></span>

### <span data-ttu-id="1e3c5-141">IotHub. m a m a 모듈 []</span><span class="sxs-lookup"><span data-stu-id="1e3c5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="1e3c5-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1e3c5-142">NOTES</span></span>

## <span data-ttu-id="1e3c5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e3c5-143">RELATED LINKS</span></span>
