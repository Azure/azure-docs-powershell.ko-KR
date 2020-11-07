---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868158"
---
# <span data-ttu-id="286d6-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="286d6-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="286d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286d6-102">SYNOPSIS</span></span>
<span data-ttu-id="286d6-103">IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="286d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="286d6-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="286d6-105">DESCRIPTION</span></span>
<span data-ttu-id="286d6-106">제공 된 IotHub 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="286d6-107">KeyNames은 고유 하지 않으므로 신중 하 게 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="286d6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="286d6-108">EXAMPLES</span></span>

### <span data-ttu-id="286d6-109">예제 1 IotHub에 키 추가</span><span class="sxs-lookup"><span data-stu-id="286d6-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="286d6-110">RegistryRead 권한이 있는 iothub "myiothub"에 대해 "mykey" 라는 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="286d6-111">변수</span><span class="sxs-lookup"><span data-stu-id="286d6-111">PARAMETERS</span></span>

### <span data-ttu-id="286d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286d6-112">-DefaultProfile</span></span>
<span data-ttu-id="286d6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="286d6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="286d6-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="286d6-114">-KeyName</span></span>
<span data-ttu-id="286d6-115">키 이름</span><span class="sxs-lookup"><span data-stu-id="286d6-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286d6-116">-이름</span><span class="sxs-lookup"><span data-stu-id="286d6-116">-Name</span></span>
<span data-ttu-id="286d6-117">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="286d6-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="286d6-118">-PrimaryKey</span></span>
<span data-ttu-id="286d6-119">기본 키</span><span class="sxs-lookup"><span data-stu-id="286d6-119">The primary key</span></span>

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

### <span data-ttu-id="286d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="286d6-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="286d6-121">Resource Group Name</span></span>

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

### <span data-ttu-id="286d6-122">-권한</span><span class="sxs-lookup"><span data-stu-id="286d6-122">-Rights</span></span>
<span data-ttu-id="286d6-123">이 IOTHub에 대 한 사용 권한</span><span class="sxs-lookup"><span data-stu-id="286d6-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="286d6-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="286d6-124">-SecondaryKey</span></span>
<span data-ttu-id="286d6-125">보조 키</span><span class="sxs-lookup"><span data-stu-id="286d6-125">The Secondary Key</span></span>

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

### <span data-ttu-id="286d6-126">-확인</span><span class="sxs-lookup"><span data-stu-id="286d6-126">-Confirm</span></span>
<span data-ttu-id="286d6-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286d6-128">-WhatIf</span></span>
<span data-ttu-id="286d6-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286d6-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286d6-131">CommonParameters</span></span>
<span data-ttu-id="286d6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="286d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286d6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286d6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286d6-134">입력</span><span class="sxs-lookup"><span data-stu-id="286d6-134">INPUTS</span></span>

### <span data-ttu-id="286d6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="286d6-135">System.String</span></span>

## <span data-ttu-id="286d6-136">출력</span><span class="sxs-lookup"><span data-stu-id="286d6-136">OUTPUTS</span></span>

### <span data-ttu-id="286d6-137">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="286d6-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="286d6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="286d6-138">NOTES</span></span>

## <span data-ttu-id="286d6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="286d6-139">RELATED LINKS</span></span>
