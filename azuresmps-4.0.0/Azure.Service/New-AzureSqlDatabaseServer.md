---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045971"
---
# <span data-ttu-id="f94dc-101">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f94dc-101">New-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="f94dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f94dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f94dc-103">Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-103">Creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="f94dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f94dc-104">SYNTAX</span></span>

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f94dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f94dc-105">DESCRIPTION</span></span>
<span data-ttu-id="f94dc-106">**AzureSqlDatabaseServer** cmdlet은 현재 구독에서 Azure SQL 데이터베이스 서버의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-106">The **New-AzureSqlDatabaseServer** cmdlet creates an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="f94dc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f94dc-107">EXAMPLES</span></span>

### <span data-ttu-id="f94dc-108">예제 1: 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="f94dc-108">Example 1: Create a server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

<span data-ttu-id="f94dc-109">이 명령은 버전 11 Azure SQL 데이터베이스 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-109">This command creates a version 11 Azure SQL Database server.</span></span>

### <span data-ttu-id="f94dc-110">예제 2: 버전 12 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="f94dc-110">Example 2: Create a version 12 server</span></span>
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

<span data-ttu-id="f94dc-111">이 명령은 버전 12 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-111">This command creates a version 12 server.</span></span>

## <span data-ttu-id="f94dc-112">변수</span><span class="sxs-lookup"><span data-stu-id="f94dc-112">PARAMETERS</span></span>

### <span data-ttu-id="f94dc-113">-관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="f94dc-113">-AdministratorLogin</span></span>
<span data-ttu-id="f94dc-114">새 Azure SQL 데이터베이스 서버에 대 한 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-114">Specifies the administrator account name for the new Azure SQL Database server.</span></span>

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

### <span data-ttu-id="f94dc-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f94dc-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f94dc-116">Azure SQL 데이터베이스 서버에 대 한 관리자 계정 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-116">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="f94dc-117">강력한 암호를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-117">You must specify a strong password.</span></span>
<span data-ttu-id="f94dc-118">자세한 내용은 Microsoft 개발자 네트워크에서 [강력한 암호](https://go.microsoft.com/fwlink/p/?LinkId=154152) 를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=154152) .</span><span class="sxs-lookup"><span data-stu-id="f94dc-118">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="f94dc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f94dc-119">-Force</span></span>
<span data-ttu-id="f94dc-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f94dc-121">-위치</span><span class="sxs-lookup"><span data-stu-id="f94dc-121">-Location</span></span>
<span data-ttu-id="f94dc-122">이 cmdlet가 서버를 만드는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-122">Specifies the location of the data center where this cmdlet creates the server.</span></span>
<span data-ttu-id="f94dc-123">자세한 내용은 azure 라이브러리에서 [Azure 지역을](https://azure.microsoft.com/regions/) 참조 하세요 https://azure.microsoft.com/regions/#services) .</span><span class="sxs-lookup"><span data-stu-id="f94dc-123">For more information, see [Azure Regions](https://azure.microsoft.com/regions/) (https://azure.microsoft.com/regions/#services) in the Azure library.</span></span>

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

### <span data-ttu-id="f94dc-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="f94dc-124">-Profile</span></span>
<span data-ttu-id="f94dc-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f94dc-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f94dc-127">-버전</span><span class="sxs-lookup"><span data-stu-id="f94dc-127">-Version</span></span>
<span data-ttu-id="f94dc-128">새 서버의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-128">Specifies the version of the new server.</span></span>
<span data-ttu-id="f94dc-129">유효한 값은 2.0 및 12.0입니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-129">Valid values are: 2.0 and 12.0.</span></span>

```yaml
Type: Single
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94dc-130">-확인</span><span class="sxs-lookup"><span data-stu-id="f94dc-130">-Confirm</span></span>
<span data-ttu-id="f94dc-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94dc-132">-WhatIf</span></span>
<span data-ttu-id="f94dc-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f94dc-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94dc-135">CommonParameters</span></span>
<span data-ttu-id="f94dc-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f94dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94dc-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f94dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94dc-138">입력</span><span class="sxs-lookup"><span data-stu-id="f94dc-138">INPUTS</span></span>

## <span data-ttu-id="f94dc-139">출력</span><span class="sxs-lookup"><span data-stu-id="f94dc-139">OUTPUTS</span></span>

### <span data-ttu-id="f94dc-140">WindowsAzure. SqlDatabase. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f94dc-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="f94dc-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f94dc-141">NOTES</span></span>

## <span data-ttu-id="f94dc-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f94dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="f94dc-143">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f94dc-143">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f94dc-144">서버 만들기</span><span class="sxs-lookup"><span data-stu-id="f94dc-144">Create Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[<span data-ttu-id="f94dc-145">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="f94dc-145">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f94dc-146">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f94dc-146">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f94dc-147">제거-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f94dc-147">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="f94dc-148">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="f94dc-148">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


