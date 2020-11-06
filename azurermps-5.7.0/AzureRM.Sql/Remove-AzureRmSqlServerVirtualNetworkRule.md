---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c0e7bc13d52633a1da5bfac2d9aec38ea3d0ee7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528763"
---
# <span data-ttu-id="54a10-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="54a10-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="54a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a10-102">SYNOPSIS</span></span>
<span data-ttu-id="54a10-103">Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54a10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54a10-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54a10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54a10-105">DESCRIPTION</span></span>
<span data-ttu-id="54a10-106">이 명령은 Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="54a10-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54a10-107">EXAMPLES</span></span>

### <span data-ttu-id="54a10-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54a10-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="54a10-109">기존 Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="54a10-110">변수</span><span class="sxs-lookup"><span data-stu-id="54a10-110">PARAMETERS</span></span>

### <span data-ttu-id="54a10-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54a10-111">-AsJob</span></span>
<span data-ttu-id="54a10-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="54a10-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a10-113">-DefaultProfile</span></span>
<span data-ttu-id="54a10-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54a10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>


```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a10-115">-ResourceGroupName</span></span>
<span data-ttu-id="54a10-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54a10-117">-ServerName</span></span>
<span data-ttu-id="54a10-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-118">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="54a10-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="54a10-120">Azure Sql Server 가상 네트워크 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="54a10-120">Azure Sql Server Virtual Network Rule name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-121">-확인</span><span class="sxs-lookup"><span data-stu-id="54a10-121">-Confirm</span></span>
<span data-ttu-id="54a10-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a10-123">-WhatIf</span></span>
<span data-ttu-id="54a10-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a10-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a10-126">CommonParameters</span></span>
<span data-ttu-id="54a10-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a10-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a10-129">입력</span><span class="sxs-lookup"><span data-stu-id="54a10-129">INPUTS</span></span>

### <span data-ttu-id="54a10-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54a10-130">System.String</span></span>

## <span data-ttu-id="54a10-131">출력</span><span class="sxs-lookup"><span data-stu-id="54a10-131">OUTPUTS</span></span>

### <span data-ttu-id="54a10-132">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="54a10-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="54a10-133">상속자</span><span class="sxs-lookup"><span data-stu-id="54a10-133">NOTES</span></span>

## <span data-ttu-id="54a10-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54a10-134">RELATED LINKS</span></span>
