---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176897"
---
# <span data-ttu-id="2dae3-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="2dae3-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="2dae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dae3-102">SYNOPSIS</span></span>
<span data-ttu-id="2dae3-103">Azure SQL Managed Instance를 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="2dae3-104">구문</span><span class="sxs-lookup"><span data-stu-id="2dae3-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dae3-105">설명</span><span class="sxs-lookup"><span data-stu-id="2dae3-105">DESCRIPTION</span></span>
<span data-ttu-id="2dae3-106">**Invoke-AzSqlInstanceFailover** cmdlet은 Azure SQL Managed Instance를 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="2dae3-107">예제</span><span class="sxs-lookup"><span data-stu-id="2dae3-107">EXAMPLES</span></span>

### <span data-ttu-id="2dae3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2dae3-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="2dae3-109">이 명령은 "ManagedInstance01"이라는 인스턴스의 주 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="2dae3-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2dae3-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="2dae3-111">이 명령은 관리되는 인스턴스 "ManagedInstance01"의 읽을 수 있는 보조 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="2dae3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dae3-112">PARAMETERS</span></span>

### <span data-ttu-id="2dae3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dae3-113">-AsJob</span></span>
<span data-ttu-id="2dae3-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2dae3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dae3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dae3-115">-DefaultProfile</span></span>
<span data-ttu-id="2dae3-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dae3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dae3-117">-Force</span></span>
<span data-ttu-id="2dae3-118">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="2dae3-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2dae3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2dae3-119">-Name</span></span>
<span data-ttu-id="2dae3-120">제거할 Azure SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dae3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dae3-121">-PassThru</span></span>
<span data-ttu-id="2dae3-122">성공한 실행 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="2dae3-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2dae3-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="2dae3-124">-ReadableSecondary</span></span>
<span data-ttu-id="2dae3-125">기본 주 복제본 대신 읽을 수 있는 보조 복제본 장애 조치(failover)</span><span class="sxs-lookup"><span data-stu-id="2dae3-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="2dae3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dae3-126">-ResourceGroupName</span></span>
<span data-ttu-id="2dae3-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dae3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dae3-128">-Confirm</span></span>
<span data-ttu-id="2dae3-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dae3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dae3-130">-WhatIf</span></span>
<span data-ttu-id="2dae3-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2dae3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dae3-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dae3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dae3-133">CommonParameters</span></span>
<span data-ttu-id="2dae3-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2dae3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dae3-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2dae3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dae3-136">입력</span><span class="sxs-lookup"><span data-stu-id="2dae3-136">INPUTS</span></span>

### <span data-ttu-id="2dae3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2dae3-137">System.String</span></span>

## <span data-ttu-id="2dae3-138">출력</span><span class="sxs-lookup"><span data-stu-id="2dae3-138">OUTPUTS</span></span>

## <span data-ttu-id="2dae3-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2dae3-139">NOTES</span></span>

## <span data-ttu-id="2dae3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dae3-140">RELATED LINKS</span></span>
