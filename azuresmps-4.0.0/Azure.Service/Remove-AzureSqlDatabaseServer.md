---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046107"
---
# <span data-ttu-id="1983e-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1983e-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="1983e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1983e-102">SYNOPSIS</span></span>
<span data-ttu-id="1983e-103">Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="1983e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1983e-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1983e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1983e-105">DESCRIPTION</span></span>
<span data-ttu-id="1983e-106">**AzureSqlDatabaseServer** cmdlet은 현재 구독에서 지정 된 Azure SQL 데이터베이스 서버의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="1983e-107">이 cmdlet은 서버의 모든 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="1983e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1983e-108">EXAMPLES</span></span>

### <span data-ttu-id="1983e-109">예제 1: 데이터베이스 서버 제거</span><span class="sxs-lookup"><span data-stu-id="1983e-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="1983e-110">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="1983e-111">변수</span><span class="sxs-lookup"><span data-stu-id="1983e-111">PARAMETERS</span></span>

### <span data-ttu-id="1983e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1983e-112">-Force</span></span>
<span data-ttu-id="1983e-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1983e-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="1983e-114">-Profile</span></span>
<span data-ttu-id="1983e-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1983e-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1983e-117">-ServerName</span></span>
<span data-ttu-id="1983e-118">이 cmdlet이 제거할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="1983e-119">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="1983e-120">-확인</span><span class="sxs-lookup"><span data-stu-id="1983e-120">-Confirm</span></span>
<span data-ttu-id="1983e-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1983e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1983e-122">-WhatIf</span></span>
<span data-ttu-id="1983e-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1983e-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1983e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1983e-125">CommonParameters</span></span>
<span data-ttu-id="1983e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1983e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1983e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1983e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1983e-128">입력</span><span class="sxs-lookup"><span data-stu-id="1983e-128">INPUTS</span></span>

### <span data-ttu-id="1983e-129">WindowsAzure. SqlDatabase. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="1983e-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="1983e-130">출력</span><span class="sxs-lookup"><span data-stu-id="1983e-130">OUTPUTS</span></span>

## <span data-ttu-id="1983e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1983e-131">NOTES</span></span>

## <span data-ttu-id="1983e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1983e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1983e-133">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="1983e-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="1983e-134">서버 삭제</span><span class="sxs-lookup"><span data-stu-id="1983e-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="1983e-135">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="1983e-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="1983e-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1983e-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1983e-137">새로운 AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1983e-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="1983e-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="1983e-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


