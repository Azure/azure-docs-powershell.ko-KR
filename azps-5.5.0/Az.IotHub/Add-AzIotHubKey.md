---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188252"
---
# <span data-ttu-id="1e124-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1e124-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="1e124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e124-102">SYNOPSIS</span></span>
<span data-ttu-id="1e124-103">IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="1e124-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e124-104">SYNTAX</span></span>

### <span data-ttu-id="1e124-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1e124-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e124-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e124-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e124-107">설명</span><span class="sxs-lookup"><span data-stu-id="1e124-107">DESCRIPTION</span></span>
<span data-ttu-id="1e124-108">제공된 IotHub에 대한 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="1e124-109">KeyNames는 고유하지 않습니다. 신중하게 관리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="1e124-110">예제</span><span class="sxs-lookup"><span data-stu-id="1e124-110">EXAMPLES</span></span>

### <span data-ttu-id="1e124-111">예제 1 IotHub에 키 추가</span><span class="sxs-lookup"><span data-stu-id="1e124-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="1e124-112">RegistryRead 권한이 있는 iothub "myiothub"에 "mykey"라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="1e124-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e124-113">PARAMETERS</span></span>

### <span data-ttu-id="1e124-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e124-114">-DefaultProfile</span></span>
<span data-ttu-id="1e124-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1e124-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e124-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="1e124-116">-HubId</span></span>
<span data-ttu-id="1e124-117">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1e124-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1e124-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1e124-118">-KeyName</span></span>
<span data-ttu-id="1e124-119">키의 이름</span><span class="sxs-lookup"><span data-stu-id="1e124-119">Name of the Key</span></span>

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

### <span data-ttu-id="1e124-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1e124-120">-Name</span></span>
<span data-ttu-id="1e124-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="1e124-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="1e124-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1e124-122">-PrimaryKey</span></span>
<span data-ttu-id="1e124-123">기본 키</span><span class="sxs-lookup"><span data-stu-id="1e124-123">The primary key</span></span>

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

### <span data-ttu-id="1e124-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e124-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e124-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1e124-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1e124-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="1e124-126">-Rights</span></span>
<span data-ttu-id="1e124-127">이 IOTHub에 대한 권한</span><span class="sxs-lookup"><span data-stu-id="1e124-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="1e124-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1e124-128">-SecondaryKey</span></span>
<span data-ttu-id="1e124-129">보조 키</span><span class="sxs-lookup"><span data-stu-id="1e124-129">The Secondary Key</span></span>

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

### <span data-ttu-id="1e124-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e124-130">-Confirm</span></span>
<span data-ttu-id="1e124-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e124-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e124-132">-WhatIf</span></span>
<span data-ttu-id="1e124-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1e124-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e124-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e124-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e124-135">CommonParameters</span></span>
<span data-ttu-id="1e124-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e124-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e124-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1e124-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e124-138">입력</span><span class="sxs-lookup"><span data-stu-id="1e124-138">INPUTS</span></span>

### <span data-ttu-id="1e124-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1e124-139">System.String</span></span>

## <span data-ttu-id="1e124-140">출력</span><span class="sxs-lookup"><span data-stu-id="1e124-140">OUTPUTS</span></span>

### <span data-ttu-id="1e124-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1e124-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="1e124-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e124-142">NOTES</span></span>

## <span data-ttu-id="1e124-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e124-143">RELATED LINKS</span></span>
