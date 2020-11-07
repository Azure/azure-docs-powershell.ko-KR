---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711054"
---
# <span data-ttu-id="e9951-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="e9951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9951-102">SYNOPSIS</span></span>
<span data-ttu-id="e9951-103">네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9951-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9951-104">SYNTAX</span></span>

### <span data-ttu-id="e9951-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="e9951-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9951-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9951-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9951-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9951-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9951-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9951-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9951-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e9951-109">DESCRIPTION</span></span>
<span data-ttu-id="e9951-110">컨테이너 네트워크 인터페이스 **구성과** 대조적으로 컨테이너 네트워크 인터페이스가 생성 되지 않은 경우 **AzureRmNetworkProfile** cmdlet은 네트워크 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="e9951-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e9951-111">EXAMPLES</span></span>

### <span data-ttu-id="e9951-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9951-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="e9951-113">이렇게 하면 리소스 그룹 rg1에서 이름이 np1 인 네트워크 프로필이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="e9951-114">변수</span><span class="sxs-lookup"><span data-stu-id="e9951-114">PARAMETERS</span></span>

### <span data-ttu-id="e9951-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9951-115">-AsJob</span></span>
<span data-ttu-id="e9951-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e9951-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9951-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9951-117">-DefaultProfile</span></span>
<span data-ttu-id="e9951-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9951-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e9951-119">-Force</span></span>
<span data-ttu-id="e9951-120">리소스를 삭제 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e9951-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e9951-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9951-121">-InputObject</span></span>
<span data-ttu-id="e9951-122">네트워크 프로필 개체.</span><span class="sxs-lookup"><span data-stu-id="e9951-122">Network profile object.</span></span>

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

### <span data-ttu-id="e9951-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e9951-123">-Name</span></span>
<span data-ttu-id="e9951-124">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-124">The name of the network profile.</span></span>

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

### <span data-ttu-id="e9951-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9951-125">-PassThru</span></span>
<span data-ttu-id="e9951-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="e9951-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e9951-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9951-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9951-128">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-128">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="e9951-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9951-129">-ResourceId</span></span>
<span data-ttu-id="e9951-130">네트워크 프로필의 Azure resource manager 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-130">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="e9951-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e9951-131">-Confirm</span></span>
<span data-ttu-id="e9951-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9951-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9951-133">-WhatIf</span></span>
<span data-ttu-id="e9951-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9951-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9951-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9951-136">CommonParameters</span></span>
<span data-ttu-id="e9951-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9951-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9951-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9951-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9951-139">입력</span><span class="sxs-lookup"><span data-stu-id="e9951-139">INPUTS</span></span>

### <span data-ttu-id="e9951-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e9951-140">System.String</span></span>

## <span data-ttu-id="e9951-141">출력</span><span class="sxs-lookup"><span data-stu-id="e9951-141">OUTPUTS</span></span>

### <span data-ttu-id="e9951-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e9951-142">System.Boolean</span></span>

## <span data-ttu-id="e9951-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e9951-143">NOTES</span></span>

## <span data-ttu-id="e9951-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9951-144">RELATED LINKS</span></span>
