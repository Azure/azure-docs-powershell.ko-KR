---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346106"
---
# <span data-ttu-id="04a15-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="04a15-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="04a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a15-102">SYNOPSIS</span></span>
<span data-ttu-id="04a15-103">TDE(투명한 데이터 암호화) 보호기</span><span class="sxs-lookup"><span data-stu-id="04a15-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="04a15-104">구문</span><span class="sxs-lookup"><span data-stu-id="04a15-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a15-105">설명</span><span class="sxs-lookup"><span data-stu-id="04a15-105">DESCRIPTION</span></span>
<span data-ttu-id="04a15-106">Get-AzSqlServerTransparentDataEncryptionProtector cmdlet은 TDE 보호기 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="04a15-107">예제</span><span class="sxs-lookup"><span data-stu-id="04a15-107">EXAMPLES</span></span>

### <span data-ttu-id="04a15-108">예제 1: TDE(투명한 데이터 암호화) 보호기</span><span class="sxs-lookup"><span data-stu-id="04a15-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="04a15-109">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 있는 ContosoServer라는 서버에 대한 TDE 보호기입니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="04a15-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="04a15-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="04a15-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="04a15-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="04a15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04a15-112">PARAMETERS</span></span>

### <span data-ttu-id="04a15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a15-113">-DefaultProfile</span></span>
<span data-ttu-id="04a15-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="04a15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04a15-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a15-115">-ResourceGroupName</span></span>
<span data-ttu-id="04a15-116">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="04a15-116">The name of the resource group</span></span>

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

### <span data-ttu-id="04a15-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04a15-117">-ServerName</span></span>
<span data-ttu-id="04a15-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="04a15-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04a15-119">-Confirm</span></span>
<span data-ttu-id="04a15-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a15-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a15-121">-WhatIf</span></span>
<span data-ttu-id="04a15-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04a15-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a15-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a15-124">CommonParameters</span></span>
<span data-ttu-id="04a15-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04a15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a15-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04a15-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a15-127">입력</span><span class="sxs-lookup"><span data-stu-id="04a15-127">INPUTS</span></span>

### <span data-ttu-id="04a15-128">System.String</span><span class="sxs-lookup"><span data-stu-id="04a15-128">System.String</span></span>

## <span data-ttu-id="04a15-129">출력</span><span class="sxs-lookup"><span data-stu-id="04a15-129">OUTPUTS</span></span>

### <span data-ttu-id="04a15-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="04a15-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="04a15-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04a15-131">NOTES</span></span>

## <span data-ttu-id="04a15-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04a15-132">RELATED LINKS</span></span>

[<span data-ttu-id="04a15-133">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="04a15-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
