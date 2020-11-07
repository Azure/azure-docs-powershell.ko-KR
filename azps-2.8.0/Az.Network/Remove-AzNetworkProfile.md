---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: ac34f2d8c2a48010792716f183a6b86cce714294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869709"
---
# <span data-ttu-id="bb6bc-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="bb6bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6bc-103">네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-103">Removes a network profile.</span></span>

## <span data-ttu-id="bb6bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb6bc-104">SYNTAX</span></span>

### <span data-ttu-id="bb6bc-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb6bc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb6bc-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb6bc-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb6bc-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb6bc-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb6bc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb6bc-108">DESCRIPTION</span></span>
<span data-ttu-id="bb6bc-109">컨테이너 네트워크 인터페이스 **구성과** 대조적으로 컨테이너 네트워크 인터페이스가 생성 되지 않은 경우 **AzNetworkProfile** cmdlet은 네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="bb6bc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bb6bc-110">EXAMPLES</span></span>

### <span data-ttu-id="bb6bc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb6bc-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="bb6bc-112">이렇게 하면 리소스 그룹 rg1에서 이름이 np1 인 네트워크 프로필이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="bb6bc-113">변수</span><span class="sxs-lookup"><span data-stu-id="bb6bc-113">PARAMETERS</span></span>

### <span data-ttu-id="bb6bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb6bc-114">-AsJob</span></span>
<span data-ttu-id="bb6bc-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bb6bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb6bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-116">-DefaultProfile</span></span>
<span data-ttu-id="bb6bc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb6bc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bb6bc-118">-Force</span></span>
<span data-ttu-id="bb6bc-119">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="bb6bc-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="bb6bc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb6bc-120">-InputObject</span></span>
<span data-ttu-id="bb6bc-121">네트워크 프로필 개체.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-121">Network profile object.</span></span>

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

### <span data-ttu-id="bb6bc-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bb6bc-122">-Name</span></span>
<span data-ttu-id="bb6bc-123">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="bb6bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb6bc-124">-PassThru</span></span>
<span data-ttu-id="bb6bc-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="bb6bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb6bc-127">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="bb6bc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6bc-128">-ResourceId</span></span>
<span data-ttu-id="bb6bc-129">네트워크 프로필의 Azure resource manager 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="bb6bc-130">-확인</span><span class="sxs-lookup"><span data-stu-id="bb6bc-130">-Confirm</span></span>
<span data-ttu-id="bb6bc-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb6bc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6bc-132">-WhatIf</span></span>
<span data-ttu-id="bb6bc-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6bc-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb6bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6bc-135">CommonParameters</span></span>
<span data-ttu-id="bb6bc-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb6bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6bc-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6bc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6bc-138">입력</span><span class="sxs-lookup"><span data-stu-id="bb6bc-138">INPUTS</span></span>

### <span data-ttu-id="bb6bc-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb6bc-139">System.String</span></span>

### <span data-ttu-id="bb6bc-140">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="bb6bc-141">출력</span><span class="sxs-lookup"><span data-stu-id="bb6bc-141">OUTPUTS</span></span>

### <span data-ttu-id="bb6bc-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bb6bc-142">System.Boolean</span></span>

## <span data-ttu-id="bb6bc-143">상속자</span><span class="sxs-lookup"><span data-stu-id="bb6bc-143">NOTES</span></span>

## <span data-ttu-id="bb6bc-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb6bc-144">RELATED LINKS</span></span>

[<span data-ttu-id="bb6bc-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="bb6bc-146">새로운 AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="bb6bc-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bb6bc-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
