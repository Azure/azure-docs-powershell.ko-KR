---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 0e83ec5266bc807f64bd231a3a423ad8cc7db190
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876726"
---
# <span data-ttu-id="01527-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="01527-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="01527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01527-102">SYNOPSIS</span></span>
<span data-ttu-id="01527-103">IotHub를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="01527-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="01527-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01527-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01527-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01527-105">DESCRIPTION</span></span>
<span data-ttu-id="01527-106">IotHub를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="01527-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="01527-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01527-107">EXAMPLES</span></span>

### <span data-ttu-id="01527-108">예제 1 IotHub 제거</span><span class="sxs-lookup"><span data-stu-id="01527-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="01527-109">"Myiothub" 이라는 IotHub를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01527-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="01527-110">변수</span><span class="sxs-lookup"><span data-stu-id="01527-110">PARAMETERS</span></span>

### <span data-ttu-id="01527-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01527-111">-DefaultProfile</span></span>
<span data-ttu-id="01527-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="01527-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01527-113">-이름</span><span class="sxs-lookup"><span data-stu-id="01527-113">-Name</span></span>
<span data-ttu-id="01527-114">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01527-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="01527-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01527-115">-ResourceGroupName</span></span>
<span data-ttu-id="01527-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="01527-116">Resource Group Name</span></span>

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

### <span data-ttu-id="01527-117">-확인</span><span class="sxs-lookup"><span data-stu-id="01527-117">-Confirm</span></span>
<span data-ttu-id="01527-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01527-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01527-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01527-119">-WhatIf</span></span>
<span data-ttu-id="01527-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01527-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01527-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01527-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01527-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01527-122">CommonParameters</span></span>
<span data-ttu-id="01527-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01527-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01527-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01527-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01527-125">입력</span><span class="sxs-lookup"><span data-stu-id="01527-125">INPUTS</span></span>

### <span data-ttu-id="01527-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01527-126">System.String</span></span>

## <span data-ttu-id="01527-127">출력</span><span class="sxs-lookup"><span data-stu-id="01527-127">OUTPUTS</span></span>

### <span data-ttu-id="01527-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="01527-128">System.Void</span></span>

## <span data-ttu-id="01527-129">상속자</span><span class="sxs-lookup"><span data-stu-id="01527-129">NOTES</span></span>

## <span data-ttu-id="01527-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01527-130">RELATED LINKS</span></span>
