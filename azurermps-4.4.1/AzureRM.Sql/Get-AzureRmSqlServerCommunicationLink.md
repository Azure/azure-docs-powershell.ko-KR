---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ed968db32505bcb3c581775d05235cc4c718dd67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532208"
---
# <span data-ttu-id="b1cdf-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b1cdf-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="b1cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cdf-103">데이터베이스 서버 간의 탄력적 데이터베이스 거래에 대 한 통신 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1cdf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1cdf-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1cdf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1cdf-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cdf-106">**AzureRmSqlServerCommunicationLink** Cmdlet은 Azure SQL database의 탄력적 데이터베이스 트랜잭션에 대 한 서버 간 통신 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="b1cdf-107">해당 링크에 대 한 속성을 보려면 서버 통신 연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="b1cdf-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b1cdf-108">EXAMPLES</span></span>

### <span data-ttu-id="b1cdf-109">예제 1: 서버에 대 한 모든 통신 링크 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1cdf-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="b1cdf-110">이 명령은 ContosoServer17 이라는 서버에 대 한 탄력적 데이터베이스 거래에 대 한 서버 간 통신 링크를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="b1cdf-111">예제 2: 서버에 대 한 특정 통신 링크 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1cdf-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="b1cdf-112">이 명령은 Link01 이라는 서버 대 서버 통신 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="b1cdf-113">변수</span><span class="sxs-lookup"><span data-stu-id="b1cdf-113">PARAMETERS</span></span>

### <span data-ttu-id="b1cdf-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="b1cdf-114">-LinkName</span></span>
<span data-ttu-id="b1cdf-115">이 cmdlet이 가져오는 서버 통신 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-115">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cdf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1cdf-116">-ResourceGroupName</span></span>
<span data-ttu-id="b1cdf-117">*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-117">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="b1cdf-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1cdf-118">-ServerName</span></span>
<span data-ttu-id="b1cdf-119">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-119">Specifies the name of a server.</span></span>
<span data-ttu-id="b1cdf-120">이 서버에는이 cmdlet이 가져오는 통신 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-120">This server contains a communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cdf-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b1cdf-121">-Confirm</span></span>
<span data-ttu-id="b1cdf-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cdf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1cdf-123">-WhatIf</span></span>
<span data-ttu-id="b1cdf-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1cdf-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cdf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cdf-126">-DefaultProfile</span></span>
<span data-ttu-id="b1cdf-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cdf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cdf-128">CommonParameters</span></span>
<span data-ttu-id="b1cdf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cdf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cdf-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cdf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cdf-131">입력</span><span class="sxs-lookup"><span data-stu-id="b1cdf-131">INPUTS</span></span>

## <span data-ttu-id="b1cdf-132">출력</span><span class="sxs-lookup"><span data-stu-id="b1cdf-132">OUTPUTS</span></span>

### <span data-ttu-id="b1cdf-133">AzureSqlServerCommunicationLinkModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="b1cdf-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="b1cdf-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b1cdf-134">NOTES</span></span>
* <span data-ttu-id="b1cdf-135">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="b1cdf-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b1cdf-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1cdf-136">RELATED LINKS</span></span>

[<span data-ttu-id="b1cdf-137">새로운 AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b1cdf-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="b1cdf-138">제거-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b1cdf-138">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="b1cdf-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b1cdf-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
