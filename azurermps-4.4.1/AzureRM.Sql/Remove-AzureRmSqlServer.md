---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537815"
---
# <span data-ttu-id="9267d-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9267d-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="9267d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9267d-102">SYNOPSIS</span></span>
<span data-ttu-id="9267d-103">Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9267d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9267d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9267d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9267d-105">DESCRIPTION</span></span>
<span data-ttu-id="9267d-106">**AzureRmSqlServer** Cmdlet은 Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="9267d-107">삭제 작업은 비동기적 이며 시간이 걸릴 수 있으므로 완전히 삭제 되는 서버에 의존 하는 추가 작업을 수행 하기 전에 작업이 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="9267d-108">예를 들어 동일한 이름을 사용 하는 새 서버를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="9267d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9267d-109">EXAMPLES</span></span>

### <span data-ttu-id="9267d-110">예제 1: 서버 제거</span><span class="sxs-lookup"><span data-stu-id="9267d-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="9267d-111">이 명령은 Server01 이라는 Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="9267d-112">변수</span><span class="sxs-lookup"><span data-stu-id="9267d-112">PARAMETERS</span></span>

### <span data-ttu-id="9267d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9267d-113">-Force</span></span>
<span data-ttu-id="9267d-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9267d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9267d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9267d-116">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9267d-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9267d-117">-ServerName</span></span>
<span data-ttu-id="9267d-118">제거할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-118">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9267d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="9267d-119">-Confirm</span></span>
<span data-ttu-id="9267d-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9267d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9267d-121">-WhatIf</span></span>
<span data-ttu-id="9267d-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9267d-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9267d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9267d-124">-DefaultProfile</span></span>
<span data-ttu-id="9267d-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9267d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9267d-126">CommonParameters</span></span>
<span data-ttu-id="9267d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9267d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9267d-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9267d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9267d-129">입력</span><span class="sxs-lookup"><span data-stu-id="9267d-129">INPUTS</span></span>

### <span data-ttu-id="9267d-130">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="9267d-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9267d-131">출력</span><span class="sxs-lookup"><span data-stu-id="9267d-131">OUTPUTS</span></span>

### <span data-ttu-id="9267d-132">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="9267d-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9267d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="9267d-133">NOTES</span></span>

## <span data-ttu-id="9267d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9267d-134">RELATED LINKS</span></span>

[<span data-ttu-id="9267d-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9267d-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="9267d-136">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9267d-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="9267d-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9267d-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="9267d-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9267d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


