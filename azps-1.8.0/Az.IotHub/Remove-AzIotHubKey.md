---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868070"
---
# <span data-ttu-id="4f4e6-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="4f4e6-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="4f4e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4e6-103">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="4f4e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f4e6-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f4e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="4f4e6-106">IotHub 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="4f4e6-107">이름이 같은 키가 여러 개 있는 경우 목록의 첫 번째 항목은 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="4f4e6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4f4e6-108">EXAMPLES</span></span>

### <span data-ttu-id="4f4e6-109">예제 1 IotHub 삭제</span><span class="sxs-lookup"><span data-stu-id="4f4e6-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="4f4e6-110">"Myiothub" 이라는 IotHub에서 iothubowner1 이라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4f4e6-111">변수</span><span class="sxs-lookup"><span data-stu-id="4f4e6-111">PARAMETERS</span></span>

### <span data-ttu-id="4f4e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4e6-112">-DefaultProfile</span></span>
<span data-ttu-id="4f4e6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f4e6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f4e6-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4f4e6-114">-KeyName</span></span>
<span data-ttu-id="4f4e6-115">키 이름</span><span class="sxs-lookup"><span data-stu-id="4f4e6-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4e6-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4f4e6-116">-Name</span></span>
<span data-ttu-id="4f4e6-117">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="4f4e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="4f4e6-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4f4e6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="4f4e6-120">-확인</span><span class="sxs-lookup"><span data-stu-id="4f4e6-120">-Confirm</span></span>
<span data-ttu-id="4f4e6-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f4e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f4e6-122">-WhatIf</span></span>
<span data-ttu-id="4f4e6-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f4e6-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f4e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4e6-125">CommonParameters</span></span>
<span data-ttu-id="4f4e6-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f4e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4e6-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4e6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4e6-128">입력</span><span class="sxs-lookup"><span data-stu-id="4f4e6-128">INPUTS</span></span>

### <span data-ttu-id="4f4e6-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f4e6-129">System.String</span></span>

## <span data-ttu-id="4f4e6-130">출력</span><span class="sxs-lookup"><span data-stu-id="4f4e6-130">OUTPUTS</span></span>

### <span data-ttu-id="4f4e6-131">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="4f4e6-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="4f4e6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4f4e6-132">NOTES</span></span>

## <span data-ttu-id="4f4e6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f4e6-133">RELATED LINKS</span></span>
