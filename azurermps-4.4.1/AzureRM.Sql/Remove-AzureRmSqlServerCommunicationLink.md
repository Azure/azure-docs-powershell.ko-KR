---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711470"
---
# <span data-ttu-id="e45e1-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e45e1-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e45e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e45e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e45e1-103">두 서버 간의 탄력적 데이터베이스 거래에 대 한 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e45e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e45e1-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e45e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e45e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e45e1-106">**AzureRmSqlServerCommunicationLink** Cmdlet은 Azure SQL 데이터베이스의 탄력적 데이터베이스 거래에 대 한 서버 간 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="e45e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e45e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e45e1-108">예제 1: 통신 링크 삭제</span><span class="sxs-lookup"><span data-stu-id="e45e1-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="e45e1-109">이 명령은 ContosoServer17에서 Link01 이라는 서버 간 통신 링크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="e45e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="e45e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e45e1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e45e1-111">-Force</span></span>
<span data-ttu-id="e45e1-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e45e1-113">-LinkName</span><span class="sxs-lookup"><span data-stu-id="e45e1-113">-LinkName</span></span>
<span data-ttu-id="e45e1-114">이 cmdlet이 삭제 하는 서버 통신 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45e1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45e1-115">-ResourceGroupName</span></span>
<span data-ttu-id="e45e1-116">*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e45e1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e45e1-117">-ServerName</span></span>
<span data-ttu-id="e45e1-118">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-118">Specifies the name of a server.</span></span>
<span data-ttu-id="e45e1-119">이 서버에는이 cmdlet이 삭제 하는 통신 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-119">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e45e1-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e45e1-120">-Confirm</span></span>
<span data-ttu-id="e45e1-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45e1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45e1-122">-WhatIf</span></span>
<span data-ttu-id="e45e1-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45e1-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45e1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45e1-125">-DefaultProfile</span></span>
<span data-ttu-id="e45e1-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e45e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45e1-127">CommonParameters</span></span>
<span data-ttu-id="e45e1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e45e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45e1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45e1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45e1-130">입력</span><span class="sxs-lookup"><span data-stu-id="e45e1-130">INPUTS</span></span>

## <span data-ttu-id="e45e1-131">출력</span><span class="sxs-lookup"><span data-stu-id="e45e1-131">OUTPUTS</span></span>

### <span data-ttu-id="e45e1-132">AzureSqlServerCommunicationLinkModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="e45e1-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e45e1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e45e1-133">NOTES</span></span>
* <span data-ttu-id="e45e1-134">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="e45e1-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e45e1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e45e1-135">RELATED LINKS</span></span>

[<span data-ttu-id="e45e1-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e45e1-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="e45e1-137">새로운 AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e45e1-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="e45e1-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e45e1-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
