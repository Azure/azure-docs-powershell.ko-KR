---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217778"
---
# <span data-ttu-id="e765e-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e765e-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="e765e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e765e-102">SYNOPSIS</span></span>
<span data-ttu-id="e765e-103">IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="e765e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e765e-104">SYNTAX</span></span>

### <span data-ttu-id="e765e-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e765e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e765e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e765e-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e765e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e765e-107">DESCRIPTION</span></span>
<span data-ttu-id="e765e-108">제공 된 IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="e765e-109">KeyNames은 고유 하지 않으므로 신중 하 게 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="e765e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e765e-110">EXAMPLES</span></span>

### <span data-ttu-id="e765e-111">예제 1 IotHub에 키 추가</span><span class="sxs-lookup"><span data-stu-id="e765e-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="e765e-112">RegistryRead 권한이 있는 iothub "myiothub"에 대해 "mykey" 라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="e765e-113">변수</span><span class="sxs-lookup"><span data-stu-id="e765e-113">PARAMETERS</span></span>

### <span data-ttu-id="e765e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e765e-114">-DefaultProfile</span></span>
<span data-ttu-id="e765e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e765e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e765e-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="e765e-116">-HubId</span></span>
<span data-ttu-id="e765e-117">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e765e-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e765e-118">-KeyName</span></span>
<span data-ttu-id="e765e-119">키 이름</span><span class="sxs-lookup"><span data-stu-id="e765e-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e765e-120">-Name</span></span>
<span data-ttu-id="e765e-121">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e765e-122">-PrimaryKey</span></span>
<span data-ttu-id="e765e-123">기본 키</span><span class="sxs-lookup"><span data-stu-id="e765e-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e765e-124">-ResourceGroupName</span></span>
<span data-ttu-id="e765e-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e765e-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-126">-권한</span><span class="sxs-lookup"><span data-stu-id="e765e-126">-Rights</span></span>
<span data-ttu-id="e765e-127">이 IOTHub에 대 한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="e765e-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e765e-128">-SecondaryKey</span></span>
<span data-ttu-id="e765e-129">보조 키</span><span class="sxs-lookup"><span data-stu-id="e765e-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e765e-130">-Confirm</span></span>
<span data-ttu-id="e765e-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e765e-132">-WhatIf</span></span>
<span data-ttu-id="e765e-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e765e-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e765e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e765e-135">CommonParameters</span></span>
<span data-ttu-id="e765e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e765e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e765e-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e765e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e765e-138">입력</span><span class="sxs-lookup"><span data-stu-id="e765e-138">INPUTS</span></span>

### <span data-ttu-id="e765e-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e765e-139">System.String</span></span>

## <span data-ttu-id="e765e-140">출력</span><span class="sxs-lookup"><span data-stu-id="e765e-140">OUTPUTS</span></span>

### <span data-ttu-id="e765e-141">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="e765e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e765e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e765e-142">NOTES</span></span>

## <span data-ttu-id="e765e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e765e-143">RELATED LINKS</span></span>
