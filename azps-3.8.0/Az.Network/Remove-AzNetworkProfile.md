---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044012"
---
# <span data-ttu-id="33d86-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="33d86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d86-102">SYNOPSIS</span></span>
<span data-ttu-id="33d86-103">네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-103">Removes a network profile.</span></span>

## <span data-ttu-id="33d86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33d86-104">SYNTAX</span></span>

### <span data-ttu-id="33d86-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="33d86-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d86-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d86-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d86-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33d86-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d86-108">설명은</span><span class="sxs-lookup"><span data-stu-id="33d86-108">DESCRIPTION</span></span>
<span data-ttu-id="33d86-109">컨테이너 네트워크 인터페이스 **구성과** 대조적으로 컨테이너 네트워크 인터페이스가 생성 되지 않은 경우 **AzNetworkProfile** cmdlet은 네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="33d86-110">예제의</span><span class="sxs-lookup"><span data-stu-id="33d86-110">EXAMPLES</span></span>

### <span data-ttu-id="33d86-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="33d86-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="33d86-112">이렇게 하면 리소스 그룹 rg1에서 이름이 np1 인 네트워크 프로필이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="33d86-113">변수</span><span class="sxs-lookup"><span data-stu-id="33d86-113">PARAMETERS</span></span>

### <span data-ttu-id="33d86-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33d86-114">-AsJob</span></span>
<span data-ttu-id="33d86-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33d86-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33d86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-116">-DefaultProfile</span></span>
<span data-ttu-id="33d86-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d86-118">-Force</span><span class="sxs-lookup"><span data-stu-id="33d86-118">-Force</span></span>
<span data-ttu-id="33d86-119">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="33d86-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="33d86-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d86-120">-InputObject</span></span>
<span data-ttu-id="33d86-121">네트워크 프로필 개체.</span><span class="sxs-lookup"><span data-stu-id="33d86-121">Network profile object.</span></span>

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

### <span data-ttu-id="33d86-122">-이름</span><span class="sxs-lookup"><span data-stu-id="33d86-122">-Name</span></span>
<span data-ttu-id="33d86-123">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="33d86-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d86-124">-PassThru</span></span>
<span data-ttu-id="33d86-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="33d86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d86-126">-ResourceGroupName</span></span>
<span data-ttu-id="33d86-127">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="33d86-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33d86-128">-ResourceId</span></span>
<span data-ttu-id="33d86-129">네트워크 프로필의 Azure resource manager 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="33d86-130">-확인</span><span class="sxs-lookup"><span data-stu-id="33d86-130">-Confirm</span></span>
<span data-ttu-id="33d86-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d86-132">-WhatIf</span></span>
<span data-ttu-id="33d86-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d86-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d86-135">CommonParameters</span></span>
<span data-ttu-id="33d86-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d86-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d86-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d86-138">입력</span><span class="sxs-lookup"><span data-stu-id="33d86-138">INPUTS</span></span>

### <span data-ttu-id="33d86-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33d86-139">System.String</span></span>

### <span data-ttu-id="33d86-140">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="33d86-141">출력</span><span class="sxs-lookup"><span data-stu-id="33d86-141">OUTPUTS</span></span>

### <span data-ttu-id="33d86-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="33d86-142">System.Boolean</span></span>

## <span data-ttu-id="33d86-143">상속자</span><span class="sxs-lookup"><span data-stu-id="33d86-143">NOTES</span></span>

## <span data-ttu-id="33d86-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33d86-144">RELATED LINKS</span></span>

[<span data-ttu-id="33d86-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="33d86-146">새로운 AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="33d86-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d86-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
