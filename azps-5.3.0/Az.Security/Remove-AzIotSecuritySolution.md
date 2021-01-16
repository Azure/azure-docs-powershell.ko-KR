---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377735"
---
# <span data-ttu-id="69ea6-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="69ea6-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="69ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="69ea6-103">IoT 보안 솔루션 삭제</span><span class="sxs-lookup"><span data-stu-id="69ea6-103">Delete IoT security solution</span></span>

## <span data-ttu-id="69ea6-104">구문</span><span class="sxs-lookup"><span data-stu-id="69ea6-104">SYNTAX</span></span>

### <span data-ttu-id="69ea6-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="69ea6-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ea6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ea6-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ea6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="69ea6-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ea6-108">설명</span><span class="sxs-lookup"><span data-stu-id="69ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="69ea6-109">Remove-AzIotSecuritySolution cmdlet은 특정 iot 보안 솔루션을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="69ea6-110">IoT 보안 솔루션은 위협을 방지하고 검색할 수 있도록 IoT 디바이스 및 IoT Hub에서 보안 데이터 및 이벤트를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="69ea6-111">예제</span><span class="sxs-lookup"><span data-stu-id="69ea6-111">EXAMPLES</span></span>

### <span data-ttu-id="69ea6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="69ea6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="69ea6-113">리소스 그룹 "MyResourceGroup"을 통해 IoT 보안 솔루션 "MySample"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="69ea6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69ea6-114">PARAMETERS</span></span>

### <span data-ttu-id="69ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="69ea6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ea6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69ea6-117">-InputObject</span></span>
<span data-ttu-id="69ea6-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="69ea6-119">-Name</span></span>
<span data-ttu-id="69ea6-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ea6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ea6-121">-PassThru</span></span>
<span data-ttu-id="69ea6-122">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="69ea6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ea6-123">-ResourceGroupName</span></span>
<span data-ttu-id="69ea6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ea6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ea6-125">-ResourceId</span></span>
<span data-ttu-id="69ea6-126">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69ea6-127">-Confirm</span></span>
<span data-ttu-id="69ea6-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ea6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ea6-129">-WhatIf</span></span>
<span data-ttu-id="69ea6-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="69ea6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ea6-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ea6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ea6-132">CommonParameters</span></span>
<span data-ttu-id="69ea6-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="69ea6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ea6-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="69ea6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ea6-135">입력</span><span class="sxs-lookup"><span data-stu-id="69ea6-135">INPUTS</span></span>

### <span data-ttu-id="69ea6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="69ea6-136">System.String</span></span>

### <span data-ttu-id="69ea6-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="69ea6-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="69ea6-138">출력</span><span class="sxs-lookup"><span data-stu-id="69ea6-138">OUTPUTS</span></span>

### <span data-ttu-id="69ea6-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69ea6-139">System.Boolean</span></span>

## <span data-ttu-id="69ea6-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="69ea6-140">NOTES</span></span>

## <span data-ttu-id="69ea6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69ea6-141">RELATED LINKS</span></span>
