---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045969"
---
# <span data-ttu-id="5fb8f-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fb8f-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="5fb8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb8f-103">Azure SQL 데이터베이스 서버에서 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="5fb8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fb8f-104">SYNTAX</span></span>

### <span data-ttu-id="5fb8f-105">IpRange (기본값)</span><span class="sxs-lookup"><span data-stu-id="5fb8f-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb8f-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="5fb8f-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb8f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5fb8f-107">DESCRIPTION</span></span>
<span data-ttu-id="5fb8f-108">**AzureSqlDatabaseServerFirewallRule** cmdlet은 현재 구독에 있는 지정 된 Azure SQL 데이터베이스 서버 인스턴스에서 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="5fb8f-109">*StartIpAddress* 및 *EndIpAddress* 매개 변수를 사용 하 여이 규칙이 Azure SQL 데이터베이스 서버에 연결할 수 있도록 허용 하는 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="5fb8f-110">*AllowAllAzureServices* 매개 변수를 지정 하 여 서버에 대 한 Azure 연결을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="5fb8f-111">규칙에 0.0.0.0의 시작 및 종료 IP 주소 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="5fb8f-112">방화벽 규칙 이름을 지정 하지 않으면이 cmdlet은 기본 이름 AllowAllAzureServices를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="5fb8f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5fb8f-113">EXAMPLES</span></span>

### <span data-ttu-id="5fb8f-114">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5fb8f-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="5fb8f-115">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 방화벽 규칙 FirewallRule24를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5fb8f-116">명령이 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="5fb8f-117">예제 2: 모든 Azure 서비스를 허용 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5fb8f-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="5fb8f-118">이 명령은 Azure 연결을 허용 하는 lpqd0zbr8y 이라는 서버에서 AzureConnections 라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="5fb8f-119">예제 3: 기본 이름을 사용 하는 모든 Azure 서비스에 사용할 수 있는 규칙 만들기 기본 이름을 사용 하는 모든 Azure 서비스를 허용 하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5fb8f-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="5fb8f-120">이 명령은 Azure 연결을 허용 하는 lpqd0zbr8y 이라는 지정 된 서버에 대 한 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="5fb8f-121">명령이 기본 규칙 이름 AllowAllAzureServices를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="5fb8f-122">변수</span><span class="sxs-lookup"><span data-stu-id="5fb8f-122">PARAMETERS</span></span>

### <span data-ttu-id="5fb8f-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="5fb8f-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="5fb8f-124">이 방화벽 규칙이 모든 Azure IP 주소에서 서버에 액세스할 수 있도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb8f-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5fb8f-125">-EndIpAddress</span></span>
<span data-ttu-id="5fb8f-126">이 규칙에 대 한 IP 주소 범위의 끝 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb8f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5fb8f-127">-Force</span></span>
<span data-ttu-id="5fb8f-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5fb8f-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="5fb8f-129">-Profile</span></span>
<span data-ttu-id="5fb8f-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fb8f-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fb8f-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5fb8f-132">-RuleName</span></span>
<span data-ttu-id="5fb8f-133">새 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb8f-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fb8f-134">-ServerName</span></span>
<span data-ttu-id="5fb8f-135">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-135">Specifies the name of a server.</span></span>
<span data-ttu-id="5fb8f-136">이 cmdlet은이 cmdlet이 지정 하는 서버에서 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="5fb8f-137">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="5fb8f-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5fb8f-138">-StartIpAddress</span></span>
<span data-ttu-id="5fb8f-139">방화벽 규칙에 대 한 IP 주소 범위의 시작 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb8f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="5fb8f-140">-Confirm</span></span>
<span data-ttu-id="5fb8f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb8f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb8f-142">-WhatIf</span></span>
<span data-ttu-id="5fb8f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb8f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb8f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb8f-145">CommonParameters</span></span>
<span data-ttu-id="5fb8f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb8f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb8f-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb8f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb8f-148">입력</span><span class="sxs-lookup"><span data-stu-id="5fb8f-148">INPUTS</span></span>

## <span data-ttu-id="5fb8f-149">출력</span><span class="sxs-lookup"><span data-stu-id="5fb8f-149">OUTPUTS</span></span>

### <span data-ttu-id="5fb8f-150">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="5fb8f-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="5fb8f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="5fb8f-151">NOTES</span></span>

## <span data-ttu-id="5fb8f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fb8f-152">RELATED LINKS</span></span>

[<span data-ttu-id="5fb8f-153">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="5fb8f-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5fb8f-154">방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="5fb8f-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="5fb8f-155">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="5fb8f-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5fb8f-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fb8f-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="5fb8f-157">제거-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fb8f-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="5fb8f-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5fb8f-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


