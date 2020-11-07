---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869894"
---
# <span data-ttu-id="246b1-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="246b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="246b1-102">SYNOPSIS</span></span>
<span data-ttu-id="246b1-103">새 네트워크 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-103">Creates a new network profile.</span></span>

## <span data-ttu-id="246b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="246b1-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="246b1-105">DESCRIPTION</span></span>
<span data-ttu-id="246b1-106">**AzNetworkProfile** cmdlet은 새 네트워크 프로필 최상위 수준 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="246b1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="246b1-107">EXAMPLES</span></span>

### <span data-ttu-id="246b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="246b1-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="246b1-109">새 네트워크 프로필 상위 수준 리소스가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="246b1-110">변수</span><span class="sxs-lookup"><span data-stu-id="246b1-110">PARAMETERS</span></span>

### <span data-ttu-id="246b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="246b1-111">-AsJob</span></span>
<span data-ttu-id="246b1-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="246b1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="246b1-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="246b1-113">-ContainerNicConfig</span></span>
<span data-ttu-id="246b1-114">이 네트워크 프로필에 추가할 컨테이너 네트워크 인터페이스 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-115">-DefaultProfile</span></span>
<span data-ttu-id="246b1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="246b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="246b1-117">-Force</span></span>
<span data-ttu-id="246b1-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="246b1-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="246b1-119">-위치</span><span class="sxs-lookup"><span data-stu-id="246b1-119">-Location</span></span>
<span data-ttu-id="246b1-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="246b1-121">-Name</span></span>
<span data-ttu-id="246b1-122">네트워크 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="246b1-124">네트워크 프로필의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b1-125">태그</span><span class="sxs-lookup"><span data-stu-id="246b1-125">-Tag</span></span>
<span data-ttu-id="246b1-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b1-127">-확인</span><span class="sxs-lookup"><span data-stu-id="246b1-127">-Confirm</span></span>
<span data-ttu-id="246b1-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246b1-129">-WhatIf</span></span>
<span data-ttu-id="246b1-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246b1-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246b1-132">CommonParameters</span></span>
<span data-ttu-id="246b1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="246b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246b1-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246b1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246b1-135">입력</span><span class="sxs-lookup"><span data-stu-id="246b1-135">INPUTS</span></span>

### <span data-ttu-id="246b1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="246b1-136">System.String</span></span>

### <span data-ttu-id="246b1-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="246b1-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="246b1-138">PSContainerNetworkInterfaceConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="246b1-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="246b1-139">출력</span><span class="sxs-lookup"><span data-stu-id="246b1-139">OUTPUTS</span></span>

### <span data-ttu-id="246b1-140">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="246b1-141">상속자</span><span class="sxs-lookup"><span data-stu-id="246b1-141">NOTES</span></span>

## <span data-ttu-id="246b1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="246b1-142">RELATED LINKS</span></span>

[<span data-ttu-id="246b1-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="246b1-144">제거-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="246b1-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="246b1-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
