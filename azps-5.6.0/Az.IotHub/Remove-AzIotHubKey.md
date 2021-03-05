---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983488"
---
# <span data-ttu-id="31acb-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="31acb-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="31acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31acb-102">SYNOPSIS</span></span>
<span data-ttu-id="31acb-103">IotHub 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="31acb-104">구문</span><span class="sxs-lookup"><span data-stu-id="31acb-104">SYNTAX</span></span>

### <span data-ttu-id="31acb-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="31acb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31acb-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31acb-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31acb-107">설명</span><span class="sxs-lookup"><span data-stu-id="31acb-107">DESCRIPTION</span></span>
<span data-ttu-id="31acb-108">IotHub 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="31acb-109">이름이 같은 키가 여러 개 있는 경우 목록의 첫 키가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="31acb-110">예제</span><span class="sxs-lookup"><span data-stu-id="31acb-110">EXAMPLES</span></span>

### <span data-ttu-id="31acb-111">예제 1 IotHub 삭제</span><span class="sxs-lookup"><span data-stu-id="31acb-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="31acb-112">"myiothub"라는 IotHub에서 iothubowner1이라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="31acb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="31acb-113">PARAMETERS</span></span>

### <span data-ttu-id="31acb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31acb-114">-DefaultProfile</span></span>
<span data-ttu-id="31acb-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31acb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31acb-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="31acb-116">-HubId</span></span>
<span data-ttu-id="31acb-117">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="31acb-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="31acb-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="31acb-118">-KeyName</span></span>
<span data-ttu-id="31acb-119">키의 이름</span><span class="sxs-lookup"><span data-stu-id="31acb-119">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31acb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="31acb-120">-Name</span></span>
<span data-ttu-id="31acb-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="31acb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="31acb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31acb-122">-ResourceGroupName</span></span>
<span data-ttu-id="31acb-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="31acb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="31acb-124">-확인</span><span class="sxs-lookup"><span data-stu-id="31acb-124">-Confirm</span></span>
<span data-ttu-id="31acb-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31acb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31acb-126">-WhatIf</span></span>
<span data-ttu-id="31acb-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31acb-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31acb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31acb-129">CommonParameters</span></span>
<span data-ttu-id="31acb-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31acb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31acb-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="31acb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31acb-132">입력</span><span class="sxs-lookup"><span data-stu-id="31acb-132">INPUTS</span></span>

### <span data-ttu-id="31acb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="31acb-133">System.String</span></span>

## <span data-ttu-id="31acb-134">출력</span><span class="sxs-lookup"><span data-stu-id="31acb-134">OUTPUTS</span></span>

### <span data-ttu-id="31acb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="31acb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="31acb-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31acb-136">NOTES</span></span>

## <span data-ttu-id="31acb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31acb-137">RELATED LINKS</span></span>
