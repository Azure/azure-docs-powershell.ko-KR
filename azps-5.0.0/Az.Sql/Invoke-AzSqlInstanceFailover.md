---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215656"
---
# <span data-ttu-id="1dc4f-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="1dc4f-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="1dc4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc4f-103">Azure SQL 관리 인스턴스를 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="1dc4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dc4f-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dc4f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1dc4f-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc4f-106">**AzSqlInstanceFailover** Cmdlet은 Azure SQL 관리 인스턴스를 장애 조치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="1dc4f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1dc4f-107">EXAMPLES</span></span>

### <span data-ttu-id="1dc4f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dc4f-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="1dc4f-109">이 명령은 "ManagedInstance01" 인스턴스의 주 복제본에 대 한 장애 조치를 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="1dc4f-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="1dc4f-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="1dc4f-111">이 명령은 관리 되는 인스턴스 "ManagedInstance01"의 읽을 수 있는 보조 복제본의 장애 조치를 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="1dc4f-112">변수</span><span class="sxs-lookup"><span data-stu-id="1dc4f-112">PARAMETERS</span></span>

### <span data-ttu-id="1dc4f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc4f-113">-AsJob</span></span>
<span data-ttu-id="1dc4f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1dc4f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc4f-115">-DefaultProfile</span></span>
<span data-ttu-id="1dc4f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc4f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc4f-117">-Force</span></span>
<span data-ttu-id="1dc4f-118">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="1dc4f-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1dc4f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1dc4f-119">-Name</span></span>
<span data-ttu-id="1dc4f-120">제거할 Azure SQL instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="1dc4f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc4f-121">-PassThru</span></span>
<span data-ttu-id="1dc4f-122">성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="1dc4f-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1dc4f-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="1dc4f-124">-ReadableSecondary</span></span>
<span data-ttu-id="1dc4f-125">기본 주 복제본 대신 읽을 수 있는 보조 복제본을 장애 조치</span><span class="sxs-lookup"><span data-stu-id="1dc4f-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="1dc4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1dc4f-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dc4f-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1dc4f-128">-Confirm</span></span>
<span data-ttu-id="1dc4f-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc4f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc4f-130">-WhatIf</span></span>
<span data-ttu-id="1dc4f-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dc4f-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc4f-133">CommonParameters</span></span>
<span data-ttu-id="1dc4f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc4f-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1dc4f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc4f-136">입력</span><span class="sxs-lookup"><span data-stu-id="1dc4f-136">INPUTS</span></span>

### <span data-ttu-id="1dc4f-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1dc4f-137">System.String</span></span>

## <span data-ttu-id="1dc4f-138">출력</span><span class="sxs-lookup"><span data-stu-id="1dc4f-138">OUTPUTS</span></span>

## <span data-ttu-id="1dc4f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1dc4f-139">NOTES</span></span>

## <span data-ttu-id="1dc4f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dc4f-140">RELATED LINKS</span></span>
