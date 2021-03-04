---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 4116ddf22bb39ddfa78e07180aaf61da7e87bb7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982144"
---
# <span data-ttu-id="d5720-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d5720-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="d5720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5720-102">SYNOPSIS</span></span>
<span data-ttu-id="d5720-103">관리되는 인스턴스에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="d5720-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5720-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5720-105">설명</span><span class="sxs-lookup"><span data-stu-id="d5720-105">DESCRIPTION</span></span>
<span data-ttu-id="d5720-106">**Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet은 관리되는 인스턴스에서 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="d5720-107">예제</span><span class="sxs-lookup"><span data-stu-id="d5720-107">EXAMPLES</span></span>

### <span data-ttu-id="d5720-108">예제 1 - 관리되는 인스턴스 고급 데이터 보안을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d5720-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="d5720-109">예제 2 - 관리되는 인스턴스 리소스에서 서버 고급 데이터 보안을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d5720-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="d5720-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d5720-110">PARAMETERS</span></span>

### <span data-ttu-id="d5720-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5720-111">-DefaultProfile</span></span>
<span data-ttu-id="d5720-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5720-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5720-113">-InputObject</span></span>
<span data-ttu-id="d5720-114">고급 데이터 보안 정책 작업과 함께 사용할 관리되는 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="d5720-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="d5720-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d5720-115">-InstanceName</span></span>
<span data-ttu-id="d5720-116">SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="d5720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5720-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5720-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5720-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d5720-119">-Confirm</span></span>
<span data-ttu-id="d5720-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5720-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5720-121">-WhatIf</span></span>
<span data-ttu-id="d5720-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5720-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5720-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5720-124">CommonParameters</span></span>
<span data-ttu-id="d5720-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5720-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5720-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5720-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5720-127">입력</span><span class="sxs-lookup"><span data-stu-id="d5720-127">INPUTS</span></span>

### <span data-ttu-id="d5720-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d5720-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d5720-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5720-129">System.String</span></span>

## <span data-ttu-id="d5720-130">출력</span><span class="sxs-lookup"><span data-stu-id="d5720-130">OUTPUTS</span></span>

### <span data-ttu-id="d5720-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d5720-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d5720-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5720-132">NOTES</span></span>

## <span data-ttu-id="d5720-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5720-133">RELATED LINKS</span></span>
