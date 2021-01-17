---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375327"
---
# <span data-ttu-id="356d8-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="356d8-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="356d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356d8-102">SYNOPSIS</span></span>
<span data-ttu-id="356d8-103">관리되는 인스턴스에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="356d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="356d8-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="356d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="356d8-105">DESCRIPTION</span></span>
<span data-ttu-id="356d8-106">**Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet은 관리되는 인스턴스에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="356d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="356d8-107">EXAMPLES</span></span>

### <span data-ttu-id="356d8-108">예제 1 - 관리되는 인스턴스 고급 데이터 보안 사용 안</span><span class="sxs-lookup"><span data-stu-id="356d8-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="356d8-109">예제 2 - 관리되는 인스턴스 리소스에서 서버 고급 데이터 보안 사용 안</span><span class="sxs-lookup"><span data-stu-id="356d8-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="356d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="356d8-110">PARAMETERS</span></span>

### <span data-ttu-id="356d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356d8-111">-DefaultProfile</span></span>
<span data-ttu-id="356d8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356d8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="356d8-113">-InputObject</span></span>
<span data-ttu-id="356d8-114">고급 데이터 보안 정책 작업에 사용할 관리되는 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="356d8-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356d8-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="356d8-115">-InstanceName</span></span>
<span data-ttu-id="356d8-116">SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="356d8-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="356d8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="356d8-119">-Confirm</span></span>
<span data-ttu-id="356d8-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356d8-121">-WhatIf</span></span>
<span data-ttu-id="356d8-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="356d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356d8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356d8-124">CommonParameters</span></span>
<span data-ttu-id="356d8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="356d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356d8-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="356d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356d8-127">입력</span><span class="sxs-lookup"><span data-stu-id="356d8-127">INPUTS</span></span>

### <span data-ttu-id="356d8-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="356d8-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="356d8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="356d8-129">System.String</span></span>

## <span data-ttu-id="356d8-130">출력</span><span class="sxs-lookup"><span data-stu-id="356d8-130">OUTPUTS</span></span>

### <span data-ttu-id="356d8-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="356d8-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="356d8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="356d8-132">NOTES</span></span>

## <span data-ttu-id="356d8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="356d8-133">RELATED LINKS</span></span>
