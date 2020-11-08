---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047553"
---
# <span data-ttu-id="f9d44-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f9d44-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f9d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d44-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d44-103">Azure SQL 가상 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f9d44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9d44-104">SYNTAX</span></span>

### <span data-ttu-id="f9d44-105">Removevirtualcluster고 Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9d44-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d44-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="f9d44-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d44-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d44-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f9d44-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d44-109">**AzSqlVirtualCluster** Cmdlet은 Azure SQL 가상 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f9d44-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f9d44-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d44-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9d44-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="f9d44-112">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 VirtualCluster1 이라는 가상 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f9d44-113">변수</span><span class="sxs-lookup"><span data-stu-id="f9d44-113">PARAMETERS</span></span>

### <span data-ttu-id="f9d44-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9d44-114">-AsJob</span></span>
<span data-ttu-id="f9d44-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9d44-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9d44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d44-116">-DefaultProfile</span></span>
<span data-ttu-id="f9d44-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d44-118">-InputObject</span></span>
<span data-ttu-id="f9d44-119">제거할 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d44-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f9d44-120">-Name</span></span>
<span data-ttu-id="f9d44-121">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d44-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9d44-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d44-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d44-124">-ResourceId</span></span>
<span data-ttu-id="f9d44-125">제거할 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d44-126">-확인</span><span class="sxs-lookup"><span data-stu-id="f9d44-126">-Confirm</span></span>
<span data-ttu-id="f9d44-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d44-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d44-128">-WhatIf</span></span>
<span data-ttu-id="f9d44-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d44-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d44-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d44-131">CommonParameters</span></span>
<span data-ttu-id="f9d44-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d44-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d44-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9d44-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d44-134">입력</span><span class="sxs-lookup"><span data-stu-id="f9d44-134">INPUTS</span></span>

### <span data-ttu-id="f9d44-135">AzureSqlVirtualClusterModel/. m a m.</span><span class="sxs-lookup"><span data-stu-id="f9d44-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="f9d44-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9d44-136">System.String</span></span>

## <span data-ttu-id="f9d44-137">출력</span><span class="sxs-lookup"><span data-stu-id="f9d44-137">OUTPUTS</span></span>

### <span data-ttu-id="f9d44-138">AzureSqlVirtualClusterModel/. m a m.</span><span class="sxs-lookup"><span data-stu-id="f9d44-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f9d44-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f9d44-139">NOTES</span></span>

## <span data-ttu-id="f9d44-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9d44-140">RELATED LINKS</span></span>
