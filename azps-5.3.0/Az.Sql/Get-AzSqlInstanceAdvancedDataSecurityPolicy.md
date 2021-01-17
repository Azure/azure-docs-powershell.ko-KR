---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492361"
---
# <span data-ttu-id="47153-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="47153-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="47153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47153-102">SYNOPSIS</span></span>
<span data-ttu-id="47153-103">관리되는 인스턴스의 고급 데이터 보안 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47153-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="47153-104">구문</span><span class="sxs-lookup"><span data-stu-id="47153-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47153-105">설명</span><span class="sxs-lookup"><span data-stu-id="47153-105">DESCRIPTION</span></span>
<span data-ttu-id="47153-106">**Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet은 관리되는 인스턴스의 고급 데이터 보안 정책을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="47153-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="47153-107">예제</span><span class="sxs-lookup"><span data-stu-id="47153-107">EXAMPLES</span></span>

### <span data-ttu-id="47153-108">예제 1: 관리되는 인스턴스 고급 데이터 보안을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47153-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="47153-109">예제 2: 관리되는 인스턴스 리소스에서 관리되는 인스턴스 Advanced Data Security를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47153-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="47153-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47153-110">PARAMETERS</span></span>

### <span data-ttu-id="47153-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47153-111">-DefaultProfile</span></span>
<span data-ttu-id="47153-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47153-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47153-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47153-113">-InputObject</span></span>
<span data-ttu-id="47153-114">고급 데이터 보안 정책 작업에 사용할 관리되는 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="47153-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="47153-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="47153-115">-InstanceName</span></span>
<span data-ttu-id="47153-116">SQL 관리되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47153-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="47153-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47153-117">-ResourceGroupName</span></span>
<span data-ttu-id="47153-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47153-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="47153-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47153-119">CommonParameters</span></span>
<span data-ttu-id="47153-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47153-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47153-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47153-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47153-122">입력</span><span class="sxs-lookup"><span data-stu-id="47153-122">INPUTS</span></span>

### <span data-ttu-id="47153-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="47153-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="47153-124">System.String</span><span class="sxs-lookup"><span data-stu-id="47153-124">System.String</span></span>

## <span data-ttu-id="47153-125">출력</span><span class="sxs-lookup"><span data-stu-id="47153-125">OUTPUTS</span></span>

### <span data-ttu-id="47153-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="47153-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="47153-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47153-127">NOTES</span></span>

## <span data-ttu-id="47153-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47153-128">RELATED LINKS</span></span>
