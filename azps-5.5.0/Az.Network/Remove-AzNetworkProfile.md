---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206597"
---
# <span data-ttu-id="4be06-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="4be06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be06-102">SYNOPSIS</span></span>
<span data-ttu-id="4be06-103">네트워크 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-103">Removes a network profile.</span></span>

## <span data-ttu-id="4be06-104">구문</span><span class="sxs-lookup"><span data-stu-id="4be06-104">SYNTAX</span></span>

### <span data-ttu-id="4be06-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4be06-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be06-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4be06-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be06-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4be06-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be06-108">설명</span><span class="sxs-lookup"><span data-stu-id="4be06-108">DESCRIPTION</span></span>
<span data-ttu-id="4be06-109">컨테이너 네트워크 인터페이스(컨테이너 네트워크 인터페이스 구성과 대조)가 생성되지 않은 경우 **Remove-AzNetworkProfile** cmdlet은 네트워크 프로필을 제거합니다. </span><span class="sxs-lookup"><span data-stu-id="4be06-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="4be06-110">예제</span><span class="sxs-lookup"><span data-stu-id="4be06-110">EXAMPLES</span></span>

### <span data-ttu-id="4be06-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4be06-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="4be06-112">그러면 리소스 그룹 rg1에서 np1 이름이 있는 네트워크 프로필이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="4be06-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4be06-113">PARAMETERS</span></span>

### <span data-ttu-id="4be06-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4be06-114">-AsJob</span></span>
<span data-ttu-id="4be06-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4be06-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4be06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-116">-DefaultProfile</span></span>
<span data-ttu-id="4be06-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be06-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4be06-118">-Force</span></span>
<span data-ttu-id="4be06-119">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="4be06-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be06-120">-InputObject</span></span>
<span data-ttu-id="4be06-121">네트워크 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be06-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4be06-122">-Name</span></span>
<span data-ttu-id="4be06-123">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be06-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4be06-124">-PassThru</span></span>
<span data-ttu-id="4be06-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="4be06-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be06-126">-ResourceGroupName</span></span>
<span data-ttu-id="4be06-127">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be06-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4be06-128">-ResourceId</span></span>
<span data-ttu-id="4be06-129">네트워크 프로필의 Azure Resource Manager 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be06-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4be06-130">-Confirm</span></span>
<span data-ttu-id="4be06-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be06-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be06-132">-WhatIf</span></span>
<span data-ttu-id="4be06-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4be06-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be06-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be06-135">CommonParameters</span></span>
<span data-ttu-id="4be06-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4be06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be06-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4be06-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be06-138">입력</span><span class="sxs-lookup"><span data-stu-id="4be06-138">INPUTS</span></span>

### <span data-ttu-id="4be06-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4be06-139">System.String</span></span>

### <span data-ttu-id="4be06-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4be06-141">출력</span><span class="sxs-lookup"><span data-stu-id="4be06-141">OUTPUTS</span></span>

### <span data-ttu-id="4be06-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4be06-142">System.Boolean</span></span>

## <span data-ttu-id="4be06-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4be06-143">NOTES</span></span>

## <span data-ttu-id="4be06-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4be06-144">RELATED LINKS</span></span>

[<span data-ttu-id="4be06-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="4be06-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="4be06-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4be06-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
