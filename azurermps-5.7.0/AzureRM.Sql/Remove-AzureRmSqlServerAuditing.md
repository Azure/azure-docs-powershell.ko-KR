---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bd5d8d2c63b10ecc4aaabd5e96ab1ce844602325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529702"
---
# <span data-ttu-id="c98ca-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="c98ca-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="c98ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c98ca-103">SQL server의 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c98ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c98ca-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c98ca-105">DESCRIPTION</span></span>
<span data-ttu-id="c98ca-106">**AzureRmSqlServerAuditing** Cmdlet은 Azure SQL server의 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="c98ca-107">이 cmdlet을 사용 하려면 서버를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="c98ca-108">이 cmdlet을 실행 한 후 Azure SQL server의 데이터베이스에 대 한 감사가 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="c98ca-109">명령이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 현재 감사 정책 및 Azure SQL server 식별자를 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="c98ca-110">서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="c98ca-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c98ca-111">EXAMPLES</span></span>

### <span data-ttu-id="c98ca-112">예제 1: Azure SQL server의 감사 제거</span><span class="sxs-lookup"><span data-stu-id="c98ca-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c98ca-113">이 명령은 리소스 그룹의 Server01에 있는 모든 데이터베이스의 감사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="c98ca-114">변수</span><span class="sxs-lookup"><span data-stu-id="c98ca-114">PARAMETERS</span></span>

### <span data-ttu-id="c98ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98ca-115">-DefaultProfile</span></span>
<span data-ttu-id="c98ca-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c98ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c98ca-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c98ca-117">-PassThru</span></span>
<span data-ttu-id="c98ca-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c98ca-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c98ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="c98ca-121">Azure SQL server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="c98ca-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c98ca-122">-ServerName</span></span>
<span data-ttu-id="c98ca-123">Azure SQL server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98ca-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c98ca-124">-Confirm</span></span>
<span data-ttu-id="c98ca-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98ca-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98ca-126">-WhatIf</span></span>
<span data-ttu-id="c98ca-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98ca-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98ca-129">CommonParameters</span></span>
<span data-ttu-id="c98ca-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c98ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98ca-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98ca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98ca-132">입력</span><span class="sxs-lookup"><span data-stu-id="c98ca-132">INPUTS</span></span>

### <span data-ttu-id="c98ca-133">Microsoft. Test.sql. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c98ca-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="c98ca-134">출력</span><span class="sxs-lookup"><span data-stu-id="c98ca-134">OUTPUTS</span></span>

### <span data-ttu-id="c98ca-135">Microsoft. Test.sql. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c98ca-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="c98ca-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c98ca-136">NOTES</span></span>

## <span data-ttu-id="c98ca-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c98ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="c98ca-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c98ca-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="c98ca-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c98ca-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="c98ca-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c98ca-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


