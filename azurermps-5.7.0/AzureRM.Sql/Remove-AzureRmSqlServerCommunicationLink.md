---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 4f9abf17be9b90cb4650c6f38748702dc0955b9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529699"
---
# <span data-ttu-id="98f72-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="98f72-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="98f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f72-102">SYNOPSIS</span></span>
<span data-ttu-id="98f72-103">두 서버 간의 탄력적 데이터베이스 거래에 대 한 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98f72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98f72-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f72-105">설명은</span><span class="sxs-lookup"><span data-stu-id="98f72-105">DESCRIPTION</span></span>
<span data-ttu-id="98f72-106">**AzureRmSqlServerCommunicationLink** Cmdlet은 Azure SQL 데이터베이스의 탄력적 데이터베이스 거래에 대 한 서버 간 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="98f72-107">예제의</span><span class="sxs-lookup"><span data-stu-id="98f72-107">EXAMPLES</span></span>

### <span data-ttu-id="98f72-108">예제 1: 통신 링크 삭제</span><span class="sxs-lookup"><span data-stu-id="98f72-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="98f72-109">이 명령은 ContosoServer17에서 Link01 이라는 서버 간 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="98f72-110">변수</span><span class="sxs-lookup"><span data-stu-id="98f72-110">PARAMETERS</span></span>

### <span data-ttu-id="98f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f72-111">-DefaultProfile</span></span>
<span data-ttu-id="98f72-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="98f72-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98f72-113">-Force</span><span class="sxs-lookup"><span data-stu-id="98f72-113">-Force</span></span>
<span data-ttu-id="98f72-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98f72-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="98f72-115">-LinkName</span></span>
<span data-ttu-id="98f72-116">이 cmdlet이 삭제 하는 서버 통신 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f72-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f72-117">-ResourceGroupName</span></span>
<span data-ttu-id="98f72-118">*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="98f72-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98f72-119">-ServerName</span></span>
<span data-ttu-id="98f72-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-120">Specifies the name of a server.</span></span>
<span data-ttu-id="98f72-121">이 서버에는이 cmdlet이 삭제 하는 통신 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="98f72-122">-확인</span><span class="sxs-lookup"><span data-stu-id="98f72-122">-Confirm</span></span>
<span data-ttu-id="98f72-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f72-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f72-124">-WhatIf</span></span>
<span data-ttu-id="98f72-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f72-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f72-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f72-127">CommonParameters</span></span>
<span data-ttu-id="98f72-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f72-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f72-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f72-130">입력</span><span class="sxs-lookup"><span data-stu-id="98f72-130">INPUTS</span></span>

### <span data-ttu-id="98f72-131">않아야</span><span class="sxs-lookup"><span data-stu-id="98f72-131">None</span></span>
<span data-ttu-id="98f72-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98f72-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98f72-133">출력</span><span class="sxs-lookup"><span data-stu-id="98f72-133">OUTPUTS</span></span>

### <span data-ttu-id="98f72-134">AzureSqlServerCommunicationLinkModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="98f72-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="98f72-135">상속자</span><span class="sxs-lookup"><span data-stu-id="98f72-135">NOTES</span></span>
* <span data-ttu-id="98f72-136">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="98f72-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="98f72-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98f72-137">RELATED LINKS</span></span>

[<span data-ttu-id="98f72-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="98f72-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="98f72-139">새로운 AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="98f72-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="98f72-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="98f72-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
