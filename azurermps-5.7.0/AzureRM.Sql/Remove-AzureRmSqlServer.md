---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529703"
---
# <span data-ttu-id="7fc63-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7fc63-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="7fc63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc63-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc63-103">Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fc63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fc63-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fc63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7fc63-105">DESCRIPTION</span></span>
<span data-ttu-id="7fc63-106">**AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="7fc63-107">삭제 작업은 비동기적 이며 시간이 걸릴 수 있으므로 완전히 삭제 되는 서버에 의존 하는 추가 작업을 수행 하기 전에 작업이 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="7fc63-108">예를 들어 동일한 이름을 사용 하는 새 서버를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="7fc63-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7fc63-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc63-110">예제 1: 서버 제거</span><span class="sxs-lookup"><span data-stu-id="7fc63-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="7fc63-111">이 명령은 Server01 이라는 Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="7fc63-112">변수</span><span class="sxs-lookup"><span data-stu-id="7fc63-112">PARAMETERS</span></span>

### <span data-ttu-id="7fc63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc63-113">-DefaultProfile</span></span>
<span data-ttu-id="7fc63-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7fc63-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fc63-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7fc63-115">-Force</span></span>
<span data-ttu-id="7fc63-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7fc63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc63-117">-ResourceGroupName</span></span>
<span data-ttu-id="7fc63-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7fc63-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7fc63-119">-ServerName</span></span>
<span data-ttu-id="7fc63-120">제거할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fc63-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7fc63-121">-Confirm</span></span>
<span data-ttu-id="7fc63-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc63-123">-WhatIf</span></span>
<span data-ttu-id="7fc63-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc63-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc63-126">CommonParameters</span></span>
<span data-ttu-id="7fc63-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fc63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc63-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc63-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc63-129">입력</span><span class="sxs-lookup"><span data-stu-id="7fc63-129">INPUTS</span></span>

### <span data-ttu-id="7fc63-130">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="7fc63-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7fc63-131">출력</span><span class="sxs-lookup"><span data-stu-id="7fc63-131">OUTPUTS</span></span>

### <span data-ttu-id="7fc63-132">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="7fc63-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="7fc63-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7fc63-133">NOTES</span></span>

## <span data-ttu-id="7fc63-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fc63-134">RELATED LINKS</span></span>

[<span data-ttu-id="7fc63-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7fc63-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="7fc63-136">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7fc63-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="7fc63-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="7fc63-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="7fc63-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7fc63-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


