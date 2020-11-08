---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217696"
---
# <span data-ttu-id="bf8d6-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf8d6-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="bf8d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8d6-103">구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="bf8d6-103">Delete Configuration record</span></span>

## <span data-ttu-id="bf8d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf8d6-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf8d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8d6-106">유지 관리 구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="bf8d6-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="bf8d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="bf8d6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf8d6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="bf8d6-109">유지 관리 구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="bf8d6-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="bf8d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf8d6-110">PARAMETERS</span></span>

### <span data-ttu-id="bf8d6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf8d6-111">-AsJob</span></span>
<span data-ttu-id="bf8d6-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bf8d6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="bf8d6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf8d6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bf8d6-115">-Force</span></span>
<span data-ttu-id="bf8d6-116">확인 하지 않고 강제로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="bf8d6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="bf8d6-117">-Name</span></span>
<span data-ttu-id="bf8d6-118">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="bf8d6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf8d6-119">-PassThru</span></span>
<span data-ttu-id="bf8d6-120">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="bf8d6-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf8d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf8d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf8d6-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="bf8d6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="bf8d6-124">-Confirm</span></span>
<span data-ttu-id="bf8d6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf8d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8d6-126">-WhatIf</span></span>
<span data-ttu-id="bf8d6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf8d6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf8d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8d6-129">CommonParameters</span></span>
<span data-ttu-id="bf8d6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8d6-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8d6-132">입력</span><span class="sxs-lookup"><span data-stu-id="bf8d6-132">INPUTS</span></span>

### <span data-ttu-id="bf8d6-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf8d6-133">System.String</span></span>

## <span data-ttu-id="bf8d6-134">출력</span><span class="sxs-lookup"><span data-stu-id="bf8d6-134">OUTPUTS</span></span>

### <span data-ttu-id="bf8d6-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bf8d6-135">System.Boolean</span></span>

## <span data-ttu-id="bf8d6-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bf8d6-136">NOTES</span></span>

## <span data-ttu-id="bf8d6-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf8d6-137">RELATED LINKS</span></span>
