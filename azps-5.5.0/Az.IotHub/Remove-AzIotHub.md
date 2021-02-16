---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200089"
---
# <span data-ttu-id="9954a-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="9954a-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="9954a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9954a-102">SYNOPSIS</span></span>
<span data-ttu-id="9954a-103">IotHub를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="9954a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9954a-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9954a-105">설명</span><span class="sxs-lookup"><span data-stu-id="9954a-105">DESCRIPTION</span></span>
<span data-ttu-id="9954a-106">IotHub를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="9954a-107">예제</span><span class="sxs-lookup"><span data-stu-id="9954a-107">EXAMPLES</span></span>

### <span data-ttu-id="9954a-108">예제 1 IotHub 제거</span><span class="sxs-lookup"><span data-stu-id="9954a-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9954a-109">"myiothub"라는 IotHub를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="9954a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9954a-110">PARAMETERS</span></span>

### <span data-ttu-id="9954a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9954a-111">-DefaultProfile</span></span>
<span data-ttu-id="9954a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9954a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9954a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9954a-113">-Name</span></span>
<span data-ttu-id="9954a-114">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="9954a-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="9954a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9954a-115">-ResourceGroupName</span></span>
<span data-ttu-id="9954a-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9954a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="9954a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9954a-117">-Confirm</span></span>
<span data-ttu-id="9954a-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9954a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9954a-119">-WhatIf</span></span>
<span data-ttu-id="9954a-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9954a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9954a-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9954a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9954a-122">CommonParameters</span></span>
<span data-ttu-id="9954a-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9954a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9954a-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9954a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9954a-125">입력</span><span class="sxs-lookup"><span data-stu-id="9954a-125">INPUTS</span></span>

### <span data-ttu-id="9954a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9954a-126">System.String</span></span>

## <span data-ttu-id="9954a-127">출력</span><span class="sxs-lookup"><span data-stu-id="9954a-127">OUTPUTS</span></span>

### <span data-ttu-id="9954a-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="9954a-128">System.Void</span></span>

## <span data-ttu-id="9954a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9954a-129">NOTES</span></span>

## <span data-ttu-id="9954a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9954a-130">RELATED LINKS</span></span>
