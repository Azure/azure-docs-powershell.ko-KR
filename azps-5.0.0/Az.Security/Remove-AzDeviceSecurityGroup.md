---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216732"
---
# <span data-ttu-id="9f577-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f577-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="9f577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f577-102">SYNOPSIS</span></span>
<span data-ttu-id="9f577-103">장치 보안 그룹 삭제</span><span class="sxs-lookup"><span data-stu-id="9f577-103">Delete device security group</span></span>

## <span data-ttu-id="9f577-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f577-104">SYNTAX</span></span>

### <span data-ttu-id="9f577-105">ResourceIdLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f577-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f577-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9f577-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f577-107">리소스</span><span class="sxs-lookup"><span data-stu-id="9f577-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f577-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9f577-108">DESCRIPTION</span></span>
<span data-ttu-id="9f577-109">Remove-AzDeviceSecurityGroup cmdlet은 iot security 솔루션에 정의 된 장치 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="9f577-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9f577-110">EXAMPLES</span></span>

### <span data-ttu-id="9f577-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f577-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="9f577-112">리소스 id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 인 iot hub의 장치 보안 그룹 "MySecurityGroup" 삭제</span><span class="sxs-lookup"><span data-stu-id="9f577-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="9f577-113">변수</span><span class="sxs-lookup"><span data-stu-id="9f577-113">PARAMETERS</span></span>

### <span data-ttu-id="9f577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f577-114">-DefaultProfile</span></span>
<span data-ttu-id="9f577-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f577-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="9f577-116">-HubResourceId</span></span>
<span data-ttu-id="9f577-117">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9f577-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f577-118">-InputObject</span></span>
<span data-ttu-id="9f577-119">입력 개체</span><span class="sxs-lookup"><span data-stu-id="9f577-119">Input Object.</span></span>

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

### <span data-ttu-id="9f577-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9f577-120">-Name</span></span>
<span data-ttu-id="9f577-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-121">Resource name.</span></span>

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

### <span data-ttu-id="9f577-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f577-122">-PassThru</span></span>
<span data-ttu-id="9f577-123">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9f577-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f577-124">-ResourceId</span></span>
<span data-ttu-id="9f577-125">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9f577-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9f577-126">-Confirm</span></span>
<span data-ttu-id="9f577-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f577-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f577-128">-WhatIf</span></span>
<span data-ttu-id="9f577-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f577-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f577-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f577-131">CommonParameters</span></span>
<span data-ttu-id="9f577-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f577-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f577-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f577-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f577-134">입력</span><span class="sxs-lookup"><span data-stu-id="9f577-134">INPUTS</span></span>

### <span data-ttu-id="9f577-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f577-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="9f577-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f577-136">System.String</span></span>

## <span data-ttu-id="9f577-137">출력</span><span class="sxs-lookup"><span data-stu-id="9f577-137">OUTPUTS</span></span>

### <span data-ttu-id="9f577-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9f577-138">System.Boolean</span></span>

## <span data-ttu-id="9f577-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9f577-139">NOTES</span></span>

## <span data-ttu-id="9f577-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f577-140">RELATED LINKS</span></span>
