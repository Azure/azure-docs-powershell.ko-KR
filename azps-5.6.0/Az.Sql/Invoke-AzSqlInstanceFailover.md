---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: cde8f48ebef73e3669a82f05c2ba91a4a4e4c582
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973488"
---
# <span data-ttu-id="cd7a0-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="cd7a0-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="cd7a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7a0-103">Managed Instance에서 Azure SQL 장애 조치(Failover)를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="cd7a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd7a0-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd7a0-105">설명</span><span class="sxs-lookup"><span data-stu-id="cd7a0-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7a0-106">**Invoke-AzSqlInstanceFailover** cmdlet은 Azure SQL 장애 조치(failover)합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="cd7a0-107">예제</span><span class="sxs-lookup"><span data-stu-id="cd7a0-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7a0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd7a0-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="cd7a0-109">이 명령은 "ManagedInstance01"이라는 인스턴스의 기본 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="cd7a0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="cd7a0-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="cd7a0-111">이 명령은 관리되는 인스턴스 "ManagedInstance01"의 읽을 수 있는 보조 복제본을 장애 조치합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="cd7a0-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd7a0-112">PARAMETERS</span></span>

### <span data-ttu-id="cd7a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd7a0-113">-AsJob</span></span>
<span data-ttu-id="cd7a0-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd7a0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd7a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7a0-115">-DefaultProfile</span></span>
<span data-ttu-id="cd7a0-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cd7a0-117">-Force</span></span>
<span data-ttu-id="cd7a0-118">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="cd7a0-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cd7a0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cd7a0-119">-Name</span></span>
<span data-ttu-id="cd7a0-120">제거할 Azure SQL 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="cd7a0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd7a0-121">-PassThru</span></span>
<span data-ttu-id="cd7a0-122">성공적인 실행에서 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="cd7a0-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd7a0-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="cd7a0-124">-ReadableSecondary</span></span>
<span data-ttu-id="cd7a0-125">기본 주 복제본 대신 읽을 수 있는 보조 복제본 장애 조치(Failover)</span><span class="sxs-lookup"><span data-stu-id="cd7a0-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="cd7a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd7a0-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd7a0-128">-확인</span><span class="sxs-lookup"><span data-stu-id="cd7a0-128">-Confirm</span></span>
<span data-ttu-id="cd7a0-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7a0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7a0-130">-WhatIf</span></span>
<span data-ttu-id="cd7a0-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd7a0-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7a0-133">CommonParameters</span></span>
<span data-ttu-id="cd7a0-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7a0-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd7a0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7a0-136">입력</span><span class="sxs-lookup"><span data-stu-id="cd7a0-136">INPUTS</span></span>

### <span data-ttu-id="cd7a0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cd7a0-137">System.String</span></span>

## <span data-ttu-id="cd7a0-138">출력</span><span class="sxs-lookup"><span data-stu-id="cd7a0-138">OUTPUTS</span></span>

## <span data-ttu-id="cd7a0-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd7a0-139">NOTES</span></span>

## <span data-ttu-id="cd7a0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd7a0-140">RELATED LINKS</span></span>
