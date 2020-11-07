---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703607"
---
# <span data-ttu-id="93616-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="93616-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="93616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93616-102">SYNOPSIS</span></span>
<span data-ttu-id="93616-103">서버 장기 보존 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93616-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93616-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93616-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93616-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93616-105">DESCRIPTION</span></span>
<span data-ttu-id="93616-106">**AzureRmSqlServerBackupLongTermRetentionVault** cmdlet은이 서버에 등록 된 장기 보존 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93616-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="93616-107">자격 증명 모음은 백업 데이터를 저장 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="93616-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="93616-108">예제의</span><span class="sxs-lookup"><span data-stu-id="93616-108">EXAMPLES</span></span>

## <span data-ttu-id="93616-109">변수</span><span class="sxs-lookup"><span data-stu-id="93616-109">PARAMETERS</span></span>

### <span data-ttu-id="93616-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93616-110">-ResourceGroupName</span></span>
<span data-ttu-id="93616-111">서버를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93616-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="93616-112">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93616-112">-ServerName</span></span>
<span data-ttu-id="93616-113">이 cmdlet이 자격 증명 모음을 가져오는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93616-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="93616-114">-확인</span><span class="sxs-lookup"><span data-stu-id="93616-114">-Confirm</span></span>
<span data-ttu-id="93616-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93616-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93616-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93616-116">-WhatIf</span></span>
<span data-ttu-id="93616-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93616-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93616-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93616-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93616-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93616-119">-DefaultProfile</span></span>
<span data-ttu-id="93616-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93616-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93616-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93616-121">CommonParameters</span></span>
<span data-ttu-id="93616-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93616-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93616-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93616-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93616-124">입력</span><span class="sxs-lookup"><span data-stu-id="93616-124">INPUTS</span></span>

## <span data-ttu-id="93616-125">출력</span><span class="sxs-lookup"><span data-stu-id="93616-125">OUTPUTS</span></span>

## <span data-ttu-id="93616-126">상속자</span><span class="sxs-lookup"><span data-stu-id="93616-126">NOTES</span></span>

## <span data-ttu-id="93616-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93616-127">RELATED LINKS</span></span>

[<span data-ttu-id="93616-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="93616-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="93616-129">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="93616-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

