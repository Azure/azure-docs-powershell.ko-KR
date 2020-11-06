---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 174bccd7b682c1c4922a5ca7b6bbfbd406667df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527255"
---
# <span data-ttu-id="7c419-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7c419-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="7c419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c419-102">SYNOPSIS</span></span>
<span data-ttu-id="7c419-103">TDE (투명 데이터 암호화) 보호기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c419-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c419-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c419-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c419-105">DESCRIPTION</span></span>
<span data-ttu-id="7c419-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet은 TDE 프로텍터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="7c419-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c419-107">EXAMPLES</span></span>

### <span data-ttu-id="7c419-108">--------------------------예제 1: TDE (투명 데이터 암호화) 보호기를 가져옵니다--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c419-108">--------------------------  Example 1: Get the Transparent Data Encryption (TDE) protector  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="7c419-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹의 ContosoServer 이라는 서버에 대 한 TDE 프로텍터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="7c419-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="7c419-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="7c419-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="7c419-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="7c419-112">변수</span><span class="sxs-lookup"><span data-stu-id="7c419-112">PARAMETERS</span></span>

### <span data-ttu-id="7c419-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c419-113">-ResourceGroupName</span></span>
<span data-ttu-id="7c419-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-114">The name of the resource group</span></span>

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

### <span data-ttu-id="7c419-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c419-115">-ServerName</span></span>
<span data-ttu-id="7c419-116">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7c419-117">-확인</span><span class="sxs-lookup"><span data-stu-id="7c419-117">-Confirm</span></span>
<span data-ttu-id="7c419-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c419-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c419-119">-WhatIf</span></span>
<span data-ttu-id="7c419-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c419-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c419-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c419-122">-DefaultProfile</span></span>
<span data-ttu-id="7c419-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c419-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c419-124">CommonParameters</span></span>
<span data-ttu-id="7c419-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c419-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c419-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c419-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c419-127">입력</span><span class="sxs-lookup"><span data-stu-id="7c419-127">INPUTS</span></span>

### <span data-ttu-id="7c419-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c419-128">System.String</span></span>

## <span data-ttu-id="7c419-129">출력</span><span class="sxs-lookup"><span data-stu-id="7c419-129">OUTPUTS</span></span>

### <span data-ttu-id="7c419-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="7c419-130">System.Object</span></span>

## <span data-ttu-id="7c419-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7c419-131">NOTES</span></span>

## <span data-ttu-id="7c419-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c419-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c419-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7c419-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
