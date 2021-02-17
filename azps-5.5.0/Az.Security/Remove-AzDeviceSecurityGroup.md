---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208309"
---
# <span data-ttu-id="af193-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="af193-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="af193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af193-102">SYNOPSIS</span></span>
<span data-ttu-id="af193-103">디바이스 보안 그룹 삭제</span><span class="sxs-lookup"><span data-stu-id="af193-103">Delete device security group</span></span>

## <span data-ttu-id="af193-104">구문</span><span class="sxs-lookup"><span data-stu-id="af193-104">SYNTAX</span></span>

### <span data-ttu-id="af193-105">ResourceIdLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="af193-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af193-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="af193-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af193-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af193-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af193-108">설명</span><span class="sxs-lookup"><span data-stu-id="af193-108">DESCRIPTION</span></span>
<span data-ttu-id="af193-109">이 Remove-AzDeviceSecurityGroup cmdlet은 iot 보안 솔루션에 정의된 디바이스 보안 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="af193-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="af193-110">예제</span><span class="sxs-lookup"><span data-stu-id="af193-110">EXAMPLES</span></span>

### <span data-ttu-id="af193-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="af193-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="af193-112">리소스 ID가 "/subscriptions/XXXXXXXXX-XXXXX-XXXXX-XXXXXX-XXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"인 iot Hub의 디바이스 보안 그룹 "MySecurityGroup"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="af193-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="af193-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af193-113">PARAMETERS</span></span>

### <span data-ttu-id="af193-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af193-114">-DefaultProfile</span></span>
<span data-ttu-id="af193-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af193-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af193-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="af193-116">-HubResourceId</span></span>
<span data-ttu-id="af193-117">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af193-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af193-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af193-118">-InputObject</span></span>
<span data-ttu-id="af193-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="af193-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af193-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af193-120">-Name</span></span>
<span data-ttu-id="af193-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af193-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af193-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af193-122">-PassThru</span></span>
<span data-ttu-id="af193-123">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="af193-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="af193-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af193-124">-ResourceId</span></span>
<span data-ttu-id="af193-125">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af193-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="af193-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af193-126">-Confirm</span></span>
<span data-ttu-id="af193-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af193-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af193-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af193-128">-WhatIf</span></span>
<span data-ttu-id="af193-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af193-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af193-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af193-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af193-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af193-131">CommonParameters</span></span>
<span data-ttu-id="af193-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af193-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af193-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af193-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af193-134">입력</span><span class="sxs-lookup"><span data-stu-id="af193-134">INPUTS</span></span>

### <span data-ttu-id="af193-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="af193-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="af193-136">System.String</span><span class="sxs-lookup"><span data-stu-id="af193-136">System.String</span></span>

## <span data-ttu-id="af193-137">출력</span><span class="sxs-lookup"><span data-stu-id="af193-137">OUTPUTS</span></span>

### <span data-ttu-id="af193-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af193-138">System.Boolean</span></span>

## <span data-ttu-id="af193-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af193-139">NOTES</span></span>

## <span data-ttu-id="af193-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af193-140">RELATED LINKS</span></span>
