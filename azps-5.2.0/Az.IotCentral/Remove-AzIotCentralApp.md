---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354974"
---
# <span data-ttu-id="68eb0-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="68eb0-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="68eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="68eb0-103">IoT Central 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="68eb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="68eb0-104">SYNTAX</span></span>

### <span data-ttu-id="68eb0-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="68eb0-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68eb0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68eb0-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68eb0-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="68eb0-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68eb0-108">설명</span><span class="sxs-lookup"><span data-stu-id="68eb0-108">DESCRIPTION</span></span>
<span data-ttu-id="68eb0-109">기존 IoT Central 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="68eb0-110">예제</span><span class="sxs-lookup"><span data-stu-id="68eb0-110">EXAMPLES</span></span>

### <span data-ttu-id="68eb0-111">예제 1 삭제 및 IoT Central 애플리케이션</span><span class="sxs-lookup"><span data-stu-id="68eb0-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="68eb0-112">제공된 IoT Central 애플리케이션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="68eb0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68eb0-113">PARAMETERS</span></span>

### <span data-ttu-id="68eb0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68eb0-114">-AsJob</span></span>
<span data-ttu-id="68eb0-115">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="68eb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68eb0-116">-DefaultProfile</span></span>
<span data-ttu-id="68eb0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68eb0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68eb0-118">-InputObject</span></span>
<span data-ttu-id="68eb0-119">Iot Central 애플리케이션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68eb0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="68eb0-120">-Name</span></span>
<span data-ttu-id="68eb0-121">Iot Central 애플리케이션 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68eb0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68eb0-122">-PassThru</span></span>
<span data-ttu-id="68eb0-123">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="68eb0-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="68eb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68eb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="68eb0-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68eb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68eb0-126">-ResourceId</span></span>
<span data-ttu-id="68eb0-127">Iot Central 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68eb0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68eb0-128">-Confirm</span></span>
<span data-ttu-id="68eb0-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68eb0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68eb0-130">-WhatIf</span></span>
<span data-ttu-id="68eb0-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="68eb0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68eb0-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68eb0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68eb0-133">CommonParameters</span></span>
<span data-ttu-id="68eb0-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68eb0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68eb0-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68eb0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68eb0-136">입력</span><span class="sxs-lookup"><span data-stu-id="68eb0-136">INPUTS</span></span>

### <span data-ttu-id="68eb0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="68eb0-137">System.String</span></span>

### <span data-ttu-id="68eb0-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="68eb0-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="68eb0-139">출력</span><span class="sxs-lookup"><span data-stu-id="68eb0-139">OUTPUTS</span></span>

### <span data-ttu-id="68eb0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68eb0-140">System.Boolean</span></span>

## <span data-ttu-id="68eb0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68eb0-141">NOTES</span></span>

## <span data-ttu-id="68eb0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68eb0-142">RELATED LINKS</span></span>
