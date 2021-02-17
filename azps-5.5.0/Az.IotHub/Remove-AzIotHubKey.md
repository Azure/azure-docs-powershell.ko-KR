---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180521"
---
# <span data-ttu-id="f33ec-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f33ec-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="f33ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f33ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f33ec-103">IotHub 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="f33ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="f33ec-104">SYNTAX</span></span>

### <span data-ttu-id="f33ec-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f33ec-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f33ec-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f33ec-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f33ec-107">설명</span><span class="sxs-lookup"><span data-stu-id="f33ec-107">DESCRIPTION</span></span>
<span data-ttu-id="f33ec-108">IotHub 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="f33ec-109">이름이 같은 키가 여러 개 있는 경우 목록의 첫 번째 키가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="f33ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="f33ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f33ec-111">예제 1 IotHub 삭제</span><span class="sxs-lookup"><span data-stu-id="f33ec-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="f33ec-112">"myiothub"라는 IotHub에서 iothubowner1이라는 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f33ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f33ec-113">PARAMETERS</span></span>

### <span data-ttu-id="f33ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f33ec-114">-DefaultProfile</span></span>
<span data-ttu-id="f33ec-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f33ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f33ec-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="f33ec-116">-HubId</span></span>
<span data-ttu-id="f33ec-117">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f33ec-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f33ec-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f33ec-118">-KeyName</span></span>
<span data-ttu-id="f33ec-119">키의 이름</span><span class="sxs-lookup"><span data-stu-id="f33ec-119">Name of the Key</span></span>

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

### <span data-ttu-id="f33ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f33ec-120">-Name</span></span>
<span data-ttu-id="f33ec-121">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="f33ec-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="f33ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f33ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="f33ec-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f33ec-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f33ec-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f33ec-124">-Confirm</span></span>
<span data-ttu-id="f33ec-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f33ec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f33ec-126">-WhatIf</span></span>
<span data-ttu-id="f33ec-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f33ec-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f33ec-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f33ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33ec-129">CommonParameters</span></span>
<span data-ttu-id="f33ec-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f33ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33ec-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f33ec-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33ec-132">입력</span><span class="sxs-lookup"><span data-stu-id="f33ec-132">INPUTS</span></span>

### <span data-ttu-id="f33ec-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f33ec-133">System.String</span></span>

## <span data-ttu-id="f33ec-134">출력</span><span class="sxs-lookup"><span data-stu-id="f33ec-134">OUTPUTS</span></span>

### <span data-ttu-id="f33ec-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f33ec-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="f33ec-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f33ec-136">NOTES</span></span>

## <span data-ttu-id="f33ec-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f33ec-137">RELATED LINKS</span></span>
