---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700785"
---
# <span data-ttu-id="85cb6-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="85cb6-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="85cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="85cb6-103">ANF (Azure NetApp Files) 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85cb6-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="85cb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85cb6-104">SYNTAX</span></span>

### <span data-ttu-id="85cb6-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="85cb6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85cb6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85cb6-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85cb6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="85cb6-107">DESCRIPTION</span></span>
<span data-ttu-id="85cb6-108">**Get-AzNetAppFilesAccount** cmdlet은 anf 계정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85cb6-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="85cb6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="85cb6-109">EXAMPLES</span></span>

### <span data-ttu-id="85cb6-110">예제 1: ANF 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="85cb6-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="85cb6-111">이 명령은 MyAnfAccount 라는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85cb6-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="85cb6-112">변수</span><span class="sxs-lookup"><span data-stu-id="85cb6-112">PARAMETERS</span></span>

### <span data-ttu-id="85cb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85cb6-113">-DefaultProfile</span></span>
<span data-ttu-id="85cb6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85cb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cb6-115">-이름</span><span class="sxs-lookup"><span data-stu-id="85cb6-115">-Name</span></span>
<span data-ttu-id="85cb6-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="85cb6-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cb6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85cb6-117">-ResourceGroupName</span></span>
<span data-ttu-id="85cb6-118">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="85cb6-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85cb6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85cb6-119">-ResourceId</span></span>
<span data-ttu-id="85cb6-120">ANF 계정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="85cb6-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85cb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85cb6-121">CommonParameters</span></span>
<span data-ttu-id="85cb6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85cb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="85cb6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85cb6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85cb6-124">입력</span><span class="sxs-lookup"><span data-stu-id="85cb6-124">INPUTS</span></span>

### <span data-ttu-id="85cb6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="85cb6-125">System.String</span></span>

## <span data-ttu-id="85cb6-126">출력</span><span class="sxs-lookup"><span data-stu-id="85cb6-126">OUTPUTS</span></span>

### <span data-ttu-id="85cb6-127">Microsoft. p. p. p. p i p. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="85cb6-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="85cb6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="85cb6-128">NOTES</span></span>

## <span data-ttu-id="85cb6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85cb6-129">RELATED LINKS</span></span>
