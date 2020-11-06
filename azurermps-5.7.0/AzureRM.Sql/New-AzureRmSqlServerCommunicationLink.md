---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531608"
---
# <span data-ttu-id="1c664-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1c664-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="1c664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c664-102">SYNOPSIS</span></span>
<span data-ttu-id="1c664-103">두 SQL 데이터베이스 서버 간의 탄력적 데이터베이스 트랜잭션에 대 한 통신 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c664-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c664-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c664-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c664-105">DESCRIPTION</span></span>
<span data-ttu-id="1c664-106">**AzureRmSqlServerCommunicationLink** Cmdlet은 Azure SQL 데이터베이스에 있는 두 논리 서버 간의 탄력적 데이터베이스 트랜잭션에 대 한 통신 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="1c664-107">탄력적 데이터베이스 트랜잭션은 쌍으로 연결 된 서버 중 하나에서 데이터베이스를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="1c664-108">서버에서 두 개 이상의 링크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="1c664-109">따라서 탄력적 데이터베이스 트랜잭션은 많은 수의 서버에서 확장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="1c664-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1c664-110">EXAMPLES</span></span>

### <span data-ttu-id="1c664-111">예제 1: 통신 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="1c664-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="1c664-112">이 명령은 ContosoServer17와 ContosoServer02 사이의 Link01 이라는 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="1c664-113">변수</span><span class="sxs-lookup"><span data-stu-id="1c664-113">PARAMETERS</span></span>

### <span data-ttu-id="1c664-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c664-114">-AsJob</span></span>
<span data-ttu-id="1c664-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1c664-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="1c664-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c664-116">-DefaultProfile</span></span>
<span data-ttu-id="1c664-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c664-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c664-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="1c664-118">-LinkName</span></span>
<span data-ttu-id="1c664-119">이 cmdlet이 만드는 서버 통신 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1c664-120">-또는 서버</span><span class="sxs-lookup"><span data-stu-id="1c664-120">-PartnerServer</span></span>
<span data-ttu-id="1c664-121">이 통신 링크에 참여 하는 다른 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="1c664-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c664-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c664-123">*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="1c664-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c664-124">-ServerName</span></span>
<span data-ttu-id="1c664-125">이 cmdlet이 통신 링크를 설정 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c664-126">-확인</span><span class="sxs-lookup"><span data-stu-id="1c664-126">-Confirm</span></span>
<span data-ttu-id="1c664-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c664-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c664-128">-WhatIf</span></span>
<span data-ttu-id="1c664-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c664-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c664-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c664-131">CommonParameters</span></span>
<span data-ttu-id="1c664-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c664-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c664-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c664-134">입력</span><span class="sxs-lookup"><span data-stu-id="1c664-134">INPUTS</span></span>

### <span data-ttu-id="1c664-135">않아야</span><span class="sxs-lookup"><span data-stu-id="1c664-135">None</span></span>
<span data-ttu-id="1c664-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c664-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c664-137">출력</span><span class="sxs-lookup"><span data-stu-id="1c664-137">OUTPUTS</span></span>

### <span data-ttu-id="1c664-138">AzureSqlServerCommunicationLinkModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="1c664-138">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="1c664-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1c664-139">NOTES</span></span>
* <span data-ttu-id="1c664-140">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="1c664-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1c664-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c664-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c664-142">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1c664-142">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1c664-143">제거-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1c664-143">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1c664-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1c664-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
