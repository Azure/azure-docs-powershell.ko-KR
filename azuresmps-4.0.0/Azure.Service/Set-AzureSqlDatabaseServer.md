---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045864"
---
# <span data-ttu-id="a4eec-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="a4eec-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="a4eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4eec-102">SYNOPSIS</span></span>
<span data-ttu-id="a4eec-103">Azure SQL 데이터베이스 서버의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="a4eec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4eec-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4eec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a4eec-105">DESCRIPTION</span></span>
<span data-ttu-id="a4eec-106">**AzureSqlDatabaseServer** cmdlet은 지정 된 Azure SQL 데이터베이스 서버의 인스턴스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="a4eec-107">현재 릴리스에서는 서버에 대 한 관리자 계정 암호만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="a4eec-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a4eec-108">EXAMPLES</span></span>

### <span data-ttu-id="a4eec-109">예제 1: 서버의 암호 변경</span><span class="sxs-lookup"><span data-stu-id="a4eec-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="a4eec-110">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에 대 한 관리자 계정 암호를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="a4eec-111">변수</span><span class="sxs-lookup"><span data-stu-id="a4eec-111">PARAMETERS</span></span>

### <span data-ttu-id="a4eec-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="a4eec-112">-AdminPassword</span></span>
<span data-ttu-id="a4eec-113">Azure SQL 데이터베이스 서버에 대 한 관리자 계정 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="a4eec-114">강력한 암호를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-114">You must specify a strong password.</span></span>
<span data-ttu-id="a4eec-115">자세한 내용은 Microsoft 개발자 네트워크에서 [강력한 암호](https://go.microsoft.com/fwlink/p/?LinkId=154152) 를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=154152) .</span><span class="sxs-lookup"><span data-stu-id="a4eec-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="a4eec-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a4eec-116">-Force</span></span>
<span data-ttu-id="a4eec-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4eec-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="a4eec-118">-Profile</span></span>
<span data-ttu-id="a4eec-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4eec-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4eec-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4eec-121">-ServerName</span></span>
<span data-ttu-id="a4eec-122">이 cmdlet이 수정 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="a4eec-123">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="a4eec-124">-확인</span><span class="sxs-lookup"><span data-stu-id="a4eec-124">-Confirm</span></span>
<span data-ttu-id="a4eec-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4eec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4eec-126">-WhatIf</span></span>
<span data-ttu-id="a4eec-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4eec-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4eec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4eec-129">CommonParameters</span></span>
<span data-ttu-id="a4eec-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4eec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4eec-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4eec-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4eec-132">입력</span><span class="sxs-lookup"><span data-stu-id="a4eec-132">INPUTS</span></span>

### <span data-ttu-id="a4eec-133">WindowsAzure. SqlDatabase. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="a4eec-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="a4eec-134">출력</span><span class="sxs-lookup"><span data-stu-id="a4eec-134">OUTPUTS</span></span>

## <span data-ttu-id="a4eec-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a4eec-135">NOTES</span></span>

## <span data-ttu-id="a4eec-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4eec-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4eec-137">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a4eec-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a4eec-138">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="a4eec-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a4eec-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="a4eec-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="a4eec-140">새로운 AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="a4eec-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="a4eec-141">제거-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="a4eec-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


