---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213975"
---
# <span data-ttu-id="8e133-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8e133-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="8e133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e133-102">SYNOPSIS</span></span>
<span data-ttu-id="8e133-103">IoT security 솔루션 삭제</span><span class="sxs-lookup"><span data-stu-id="8e133-103">Delete IoT security solution</span></span>

## <span data-ttu-id="8e133-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e133-104">SYNTAX</span></span>

### <span data-ttu-id="8e133-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e133-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e133-106">리소스</span><span class="sxs-lookup"><span data-stu-id="8e133-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e133-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e133-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e133-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8e133-108">DESCRIPTION</span></span>
<span data-ttu-id="8e133-109">Remove-AzIotSecuritySolution cmdlet은 특정 iot 보안 솔루션을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="8e133-110">IoT security 솔루션은 iot 디바이스 및 iot hub의 보안 데이터 및 이벤트를 수집 하 여 위협을 방지 하 고 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="8e133-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8e133-111">EXAMPLES</span></span>

### <span data-ttu-id="8e133-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e133-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8e133-113">리소스 그룹 "MyResourceGroup"을 사용 하 여 IoT security 솔루션 "MySample" 삭제</span><span class="sxs-lookup"><span data-stu-id="8e133-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="8e133-114">변수</span><span class="sxs-lookup"><span data-stu-id="8e133-114">PARAMETERS</span></span>

### <span data-ttu-id="8e133-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e133-115">-DefaultProfile</span></span>
<span data-ttu-id="8e133-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e133-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e133-117">-InputObject</span></span>
<span data-ttu-id="8e133-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="8e133-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8e133-119">-Name</span></span>
<span data-ttu-id="8e133-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e133-121">-PassThru</span></span>
<span data-ttu-id="8e133-122">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-122">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e133-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e133-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e133-125">-ResourceId</span></span>
<span data-ttu-id="8e133-126">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-127">-확인</span><span class="sxs-lookup"><span data-stu-id="8e133-127">-Confirm</span></span>
<span data-ttu-id="8e133-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e133-129">-WhatIf</span></span>
<span data-ttu-id="8e133-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e133-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e133-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e133-132">CommonParameters</span></span>
<span data-ttu-id="8e133-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e133-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e133-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e133-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e133-135">입력</span><span class="sxs-lookup"><span data-stu-id="8e133-135">INPUTS</span></span>

### <span data-ttu-id="8e133-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e133-136">System.String</span></span>

### <span data-ttu-id="8e133-137">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="8e133-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="8e133-138">출력</span><span class="sxs-lookup"><span data-stu-id="8e133-138">OUTPUTS</span></span>

### <span data-ttu-id="8e133-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8e133-139">System.Boolean</span></span>

## <span data-ttu-id="8e133-140">상속자</span><span class="sxs-lookup"><span data-stu-id="8e133-140">NOTES</span></span>

## <span data-ttu-id="8e133-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e133-141">RELATED LINKS</span></span>
