---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386779"
---
# <span data-ttu-id="37cc9-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="37cc9-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="37cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="37cc9-103">IotHub를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="37cc9-104">구문</span><span class="sxs-lookup"><span data-stu-id="37cc9-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37cc9-105">설명</span><span class="sxs-lookup"><span data-stu-id="37cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="37cc9-106">IotHub를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="37cc9-107">예제</span><span class="sxs-lookup"><span data-stu-id="37cc9-107">EXAMPLES</span></span>

### <span data-ttu-id="37cc9-108">예제 1 IotHub 제거</span><span class="sxs-lookup"><span data-stu-id="37cc9-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="37cc9-109">"myiothub"라는 IotHub를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="37cc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37cc9-110">PARAMETERS</span></span>

### <span data-ttu-id="37cc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cc9-111">-DefaultProfile</span></span>
<span data-ttu-id="37cc9-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37cc9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37cc9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="37cc9-113">-Name</span></span>
<span data-ttu-id="37cc9-114">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="37cc9-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="37cc9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cc9-115">-ResourceGroupName</span></span>
<span data-ttu-id="37cc9-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="37cc9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="37cc9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37cc9-117">-Confirm</span></span>
<span data-ttu-id="37cc9-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cc9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cc9-119">-WhatIf</span></span>
<span data-ttu-id="37cc9-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37cc9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cc9-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cc9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cc9-122">CommonParameters</span></span>
<span data-ttu-id="37cc9-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37cc9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cc9-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="37cc9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cc9-125">입력</span><span class="sxs-lookup"><span data-stu-id="37cc9-125">INPUTS</span></span>

### <span data-ttu-id="37cc9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="37cc9-126">System.String</span></span>

## <span data-ttu-id="37cc9-127">출력</span><span class="sxs-lookup"><span data-stu-id="37cc9-127">OUTPUTS</span></span>

### <span data-ttu-id="37cc9-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="37cc9-128">System.Void</span></span>

## <span data-ttu-id="37cc9-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37cc9-129">NOTES</span></span>

## <span data-ttu-id="37cc9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37cc9-130">RELATED LINKS</span></span>
