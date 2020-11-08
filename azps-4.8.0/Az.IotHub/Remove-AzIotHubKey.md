---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056710"
---
# <span data-ttu-id="118a0-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="118a0-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="118a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="118a0-102">SYNOPSIS</span></span>
<span data-ttu-id="118a0-103">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="118a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="118a0-104">SYNTAX</span></span>

### <span data-ttu-id="118a0-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="118a0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="118a0-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="118a0-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="118a0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="118a0-107">DESCRIPTION</span></span>
<span data-ttu-id="118a0-108">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="118a0-109">이름이 같은 키가 여러 개 있는 경우 목록의 첫 번째 항목은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="118a0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="118a0-110">EXAMPLES</span></span>

### <span data-ttu-id="118a0-111">예제 1 IotHub 삭제</span><span class="sxs-lookup"><span data-stu-id="118a0-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="118a0-112">"Myiothub" 이라는 IotHub에서 iothubowner1 이라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="118a0-113">변수</span><span class="sxs-lookup"><span data-stu-id="118a0-113">PARAMETERS</span></span>

### <span data-ttu-id="118a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="118a0-114">-DefaultProfile</span></span>
<span data-ttu-id="118a0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="118a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="118a0-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="118a0-116">-HubId</span></span>
<span data-ttu-id="118a0-117">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="118a0-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="118a0-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="118a0-118">-KeyName</span></span>
<span data-ttu-id="118a0-119">키 이름</span><span class="sxs-lookup"><span data-stu-id="118a0-119">Name of the Key</span></span>

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

### <span data-ttu-id="118a0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="118a0-120">-Name</span></span>
<span data-ttu-id="118a0-121">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="118a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="118a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="118a0-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="118a0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="118a0-124">-확인</span><span class="sxs-lookup"><span data-stu-id="118a0-124">-Confirm</span></span>
<span data-ttu-id="118a0-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="118a0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="118a0-126">-WhatIf</span></span>
<span data-ttu-id="118a0-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="118a0-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="118a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118a0-129">CommonParameters</span></span>
<span data-ttu-id="118a0-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="118a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118a0-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="118a0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118a0-132">입력</span><span class="sxs-lookup"><span data-stu-id="118a0-132">INPUTS</span></span>

### <span data-ttu-id="118a0-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="118a0-133">System.String</span></span>

## <span data-ttu-id="118a0-134">출력</span><span class="sxs-lookup"><span data-stu-id="118a0-134">OUTPUTS</span></span>

### <span data-ttu-id="118a0-135">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="118a0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="118a0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="118a0-136">NOTES</span></span>

## <span data-ttu-id="118a0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="118a0-137">RELATED LINKS</span></span>
