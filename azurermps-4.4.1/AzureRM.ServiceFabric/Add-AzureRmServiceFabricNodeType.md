---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532927"
---
# <span data-ttu-id="0da7f-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0da7f-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="0da7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da7f-102">SYNOPSIS</span></span>
<span data-ttu-id="0da7f-103">기존 클러스터에 새 노드 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0da7f-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0da7f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0da7f-105">DESCRIPTION</span></span>
<span data-ttu-id="0da7f-106">기존 클러스터에 새 노드 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="0da7f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0da7f-107">EXAMPLES</span></span>

### <span data-ttu-id="0da7f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0da7f-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="0da7f-109">이 명령은 5 개 용량의 새 NodeType ' n2 '와 vm 관리자 이름이 ' adminName '으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="0da7f-110">변수</span><span class="sxs-lookup"><span data-stu-id="0da7f-110">PARAMETERS</span></span>

### <span data-ttu-id="0da7f-111">용량</span><span class="sxs-lookup"><span data-stu-id="0da7f-111">-Capacity</span></span>
<span data-ttu-id="0da7f-112">용량</span><span class="sxs-lookup"><span data-stu-id="0da7f-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0da7f-113">-Name</span></span>
<span data-ttu-id="0da7f-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0da7f-115">-NodeType</span></span>
<span data-ttu-id="0da7f-116">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-116">The node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0da7f-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-119">-티어</span><span class="sxs-lookup"><span data-stu-id="0da7f-119">-Tier</span></span>
<span data-ttu-id="0da7f-120">Vm Sku 계층.</span><span class="sxs-lookup"><span data-stu-id="0da7f-120">Vm Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0da7f-121">-DurabilityLevel</span></span>
<span data-ttu-id="0da7f-122">NodeType의 영속성 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-122">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="0da7f-123">-VmPassword</span></span>
<span data-ttu-id="0da7f-124">Vm에 대 한 로그인 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-124">The password of login to the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="0da7f-125">-VmSku</span></span>
<span data-ttu-id="0da7f-126">Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-126">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="0da7f-127">-VmUserName</span></span>
<span data-ttu-id="0da7f-128">Vm에 로그인 하는 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-128">The user name for login to Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da7f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0da7f-129">-Confirm</span></span>
<span data-ttu-id="0da7f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da7f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da7f-131">-WhatIf</span></span>
<span data-ttu-id="0da7f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0da7f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da7f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da7f-134">-DefaultProfile</span></span>
<span data-ttu-id="0da7f-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da7f-136">CommonParameters</span></span>
<span data-ttu-id="0da7f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0da7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da7f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da7f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da7f-139">입력</span><span class="sxs-lookup"><span data-stu-id="0da7f-139">INPUTS</span></span>

### <span data-ttu-id="0da7f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0da7f-140">System.String</span></span>
<span data-ttu-id="0da7f-141">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="0da7f-141">System.Int32</span></span>

## <span data-ttu-id="0da7f-142">출력</span><span class="sxs-lookup"><span data-stu-id="0da7f-142">OUTPUTS</span></span>

### <span data-ttu-id="0da7f-143">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0da7f-143">System.Object</span></span>

## <span data-ttu-id="0da7f-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0da7f-144">NOTES</span></span>

## <span data-ttu-id="0da7f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0da7f-145">RELATED LINKS</span></span>

