---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360088"
---
# <span data-ttu-id="d73ec-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d73ec-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d73ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d73ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d73ec-103">ANF(Azure NetApp Files) 백업 정책에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d73ec-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="d73ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="d73ec-104">SYNTAX</span></span>

### <span data-ttu-id="d73ec-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d73ec-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d73ec-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73ec-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d73ec-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d73ec-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d73ec-108">설명</span><span class="sxs-lookup"><span data-stu-id="d73ec-108">DESCRIPTION</span></span>
<span data-ttu-id="d73ec-109">**Get-AzNetAppFilesBackupPolicy** cmdlet은 ANF 백업 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d73ec-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="d73ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="d73ec-110">EXAMPLES</span></span>

### <span data-ttu-id="d73ec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d73ec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="d73ec-112">이 명령은 "MyAnfAccount" 계정에 대해 "MyBackupPolicy"라는 백업 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d73ec-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="d73ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d73ec-113">PARAMETERS</span></span>

### <span data-ttu-id="d73ec-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d73ec-114">-AccountName</span></span>
<span data-ttu-id="d73ec-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d73ec-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73ec-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d73ec-116">-AccountObject</span></span>
<span data-ttu-id="d73ec-117">반환할 Backup 정책을 포함하는 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d73ec-117">The Account object containing the Backup Policy to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d73ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73ec-118">-DefaultProfile</span></span>
<span data-ttu-id="d73ec-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d73ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d73ec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d73ec-120">-Name</span></span>
<span data-ttu-id="d73ec-121">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="d73ec-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="d73ec-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="d73ec-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d73ec-124">-ResourceId</span></span>
<span data-ttu-id="d73ec-125">ANF Backup 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d73ec-125">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d73ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73ec-126">CommonParameters</span></span>
<span data-ttu-id="d73ec-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d73ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73ec-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d73ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73ec-129">입력</span><span class="sxs-lookup"><span data-stu-id="d73ec-129">INPUTS</span></span>

### <span data-ttu-id="d73ec-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d73ec-130">System.String</span></span>

### <span data-ttu-id="d73ec-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d73ec-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d73ec-132">출력</span><span class="sxs-lookup"><span data-stu-id="d73ec-132">OUTPUTS</span></span>

### <span data-ttu-id="d73ec-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d73ec-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d73ec-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d73ec-134">NOTES</span></span>

## <span data-ttu-id="d73ec-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d73ec-135">RELATED LINKS</span></span>
