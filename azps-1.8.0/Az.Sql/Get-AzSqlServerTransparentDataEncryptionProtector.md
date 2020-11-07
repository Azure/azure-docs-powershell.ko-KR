---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: c1571dd5d03f82da13feec115fb9da123c6e3f69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698931"
---
# <span data-ttu-id="982ff-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="982ff-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="982ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982ff-102">SYNOPSIS</span></span>
<span data-ttu-id="982ff-103">TDE (투명 데이터 암호화) 보호기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="982ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="982ff-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="982ff-105">DESCRIPTION</span></span>
<span data-ttu-id="982ff-106">Get-AzSqlServerTransparentDataEncryptionProtector cmdlet은 TDE 프로텍터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="982ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="982ff-107">EXAMPLES</span></span>

### <span data-ttu-id="982ff-108">예제 1: TDE (투명 데이터 암호화) 보호기 가져오기</span><span class="sxs-lookup"><span data-stu-id="982ff-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="982ff-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoServer 이라는 서버에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="982ff-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="982ff-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="982ff-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="982ff-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="982ff-112">변수</span><span class="sxs-lookup"><span data-stu-id="982ff-112">PARAMETERS</span></span>

### <span data-ttu-id="982ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982ff-113">-DefaultProfile</span></span>
<span data-ttu-id="982ff-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="982ff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="982ff-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-116">The name of the resource group</span></span>

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

### <span data-ttu-id="982ff-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="982ff-117">-ServerName</span></span>
<span data-ttu-id="982ff-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="982ff-119">-확인</span><span class="sxs-lookup"><span data-stu-id="982ff-119">-Confirm</span></span>
<span data-ttu-id="982ff-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982ff-121">-WhatIf</span></span>
<span data-ttu-id="982ff-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982ff-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982ff-124">CommonParameters</span></span>
<span data-ttu-id="982ff-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="982ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982ff-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="982ff-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982ff-127">입력</span><span class="sxs-lookup"><span data-stu-id="982ff-127">INPUTS</span></span>

### <span data-ttu-id="982ff-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="982ff-128">System.String</span></span>

## <span data-ttu-id="982ff-129">출력</span><span class="sxs-lookup"><span data-stu-id="982ff-129">OUTPUTS</span></span>

### <span data-ttu-id="982ff-130">TransparentDataEncryption. AzureSqlServerTransparentDataEncryptionProtectorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="982ff-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="982ff-131">상속자</span><span class="sxs-lookup"><span data-stu-id="982ff-131">NOTES</span></span>

## <span data-ttu-id="982ff-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="982ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="982ff-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="982ff-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
